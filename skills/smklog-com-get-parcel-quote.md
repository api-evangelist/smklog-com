---
name: get-parcel-quote
description: Get live purchasable parcel shipping rates from a plain-words item description via the SMKlog quote API. Origin is a US address; destinations are the US, Canada, the UK, Germany and Australia.
---

# Get a parcel quote from SMKlog

Price one parcel from a US origin across USPS, UPS and FedEx (plus DHL Express to Germany and Australia) from a description
of the item. Box size and weight are estimated when omitted.

## Call

`POST https://quote-api.smklog.com/quote` with JSON:

```json
{
  "action": "smart_quote",
  "product": "Yamaha FG800 acoustic guitar in a hard case",
  "from_postal_code": "07102",
  "to_postal_code": "30303",
  "quantity": 1
}
```

Optional when known: `weight_kg`, `length_cm`, `width_cm`, `height_cm`
(all four together, or the estimate is used), `packaging` ("box" skips
packaging estimation), `to_country_code` (`US` default, `CA`, `GB`, `DE`,
`AU`; `to_postal_code` is then that country's postal code). `quantity` 1
is the only value priced online: more parcels, or a box over 68 kg, 274 cm on
the longest side or 419 cm of length plus girth, come back as
`mode: "freight_manager"` with empty rates and a person prices them.

## Read the answer

`mode: "parcel_label_ready"` carries up to five services in `rates`.
Two prices per rate and they are not interchangeable: `amount` is the
checkout total a customer pays, with the SMKlog fee inside it (the fee is
itemized only on the checkout receipt); `retail_amount` is the carrier's
own counter price for the same parcel where one is published (0 otherwise).
`counter_price` (when present) is the Post Office counter price for the
same parcel — the comparison anchor. No account or key is needed; requests
are rate limited per client.
