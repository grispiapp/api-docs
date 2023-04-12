---
title: Grispi Public API Gsocial Extension
---

This document should be considered as an extension of Grispi Public API document. [Grispi Public API](https://grispiapp.github.io/api-docs/) It contains some internal details for Gsocial to use public API. Grispi Public API must be read prior to this document.

## Social media external ids
Here are social media external ids:

- `us.whatsapp_id`
- `us.google_reviews_id`
- `us.twitter_id`
- `us.instagram_id`
- `us.facebook_id`
- `us.sikayet_var_id`
- `us.google_play_store_id`
- `us.apple_app_store_id`

> They are called **social id** throughout the document.

> _See `UserIdentifierField` in Public API document to learn how to use these ids._

## How social ids affect `UserIdentifierField` diagram in Public API document
At first, `us.id` is checked, as stated in diagram. If `us.id` is not sent and one of social ids is found, we enter scope of this document. User creation flow is as follows:

[![](gsocial_user_creation_diagram.jpg)](gsocial_user_creation_diagram.jpg)
