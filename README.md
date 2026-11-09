# ISO 8583 Decoder

Paste an ISO 8583 message as text and get every data element decoded into a JSON object.

**Live:** https://rocketflash-net.github.io/tlv-8535-decoder/

- Reads the MTI, the primary and secondary hex bitmaps, then each data element by its ISO 8583:1987 format (fixed, LLVAR, LLLVAR)
- QRIS switching profile: DE41 as ans16, DE43 split into merchant name, city and country, TLV in DE48 (PI, CD, MC) and DE57 (61 postal code, 62 additional data)
- Builds full dates from MMDD fields (year picked closest to today, or set it yourself) and keeps amounts exact with two decimals
- Explains MTI, processing code, MCC, currency and response code
- Flags truncated messages, bad length prefixes, leftover characters and non-numeric values
- Colour-coded message linked to the field table on hover
- Minified or pretty JSON, copy to clipboard, English and Bahasa Indonesia, light and dark theme

Everything runs in the browser. The message is never sent anywhere.

This is a learning and debugging tool. Switch specs differ, so check field layouts against your network's own spec.

---

Built by [Daniel Aldo Pratama](https://rocketflash-net.github.io/it/).
