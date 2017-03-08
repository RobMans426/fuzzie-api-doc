This replaces `valid_with` and `valid_with_text` in the Brand object under `/api/home`. They should not be used anymore. 

Instead the Brand object now has `options_for_gift_cards` and `options_for_packages` - both of them are text fields. They should be used for
display under gift cards and packages respectively.
