API relevant changes since last release / "to implement" list:

Refer to mastodon changelog and API docs for details when implementing, add or modify tests where needed

4.0.0 and beyond
----------------
* [ ] Document all the endpoints we need to add
<<<<<<< HEAD
  * [ ] [PATCH /api/v1/accounts/update_credentials HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#update_credentials) 4.1.0 - added hide_collections parameter, 4.2.0 - added indexable parameter
  * [ ] [GET /api/v1/accounts/:id/followers HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#followers) 4.0.0 - no longer requires an app token + read:accounts
  * [ ] [GET /api/v1/accounts/:id/following HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#following) 4.0.0 - no longer requires an app token + read:accounts
  * [ ] [POST /api/v1/accounts/:id/follow HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#follow) 4.0.0 - added languages
  * [ ] [POST /api/v1/accounts/:id/pin HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#pin) 4.0.0 - calling this method is now idempotent
  * [ ] [GET /api/v1/accounts/relationships HTTP/1.1](https://docs.joinmastodon.org/methods/accounts/#relationships) 4.3.0 - added with_suspended parameter
  * [ ] [GET /api/v2/filters HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#get) added in 4.0
  * [ ] [GET /api/v2/filters/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#get-one) added in 4.0
  * [ ] [POST /api/v2/filters HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#create) added in 4.0
  * [ ] [PUT /api/v2/filters/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#update) added in 4.0
  * [ ] [DELETE /api/v2/filters/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#delete) added in 4.0
  * [ ] [GET /api/v2/filters/:filter_id/keywords HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#keywords-get) added in 4.0
  * [ ] [POST /api/v2/filters/:filter_id/keywords HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#keywords-create) added in 4.0
  * [ ] [GET /api/v2/filters/keywords/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#keywords-get-one) added in 4.0
  * [ ] [PUT /api/v2/filters/keywords/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#keywords-update) added in 4.0
  * [ ] [DELETE /api/v2/filters/keywords/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#keywords-delete) added in 4.0
  * [ ] [GET /api/v2/filters/:filter_id/statuses HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#statuses-get) added in 4.0
  * [ ] [POST /api/v2/filters/:filter_id/statuses HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#statuses-add) added in 4.0
  * [ ] [GET /api/v2/filters/statuses/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#statuses-get-one) added in 4.0
  * [ ] [DELETE /api/v2/filters/statuses/:id HTTP/1.1](https://docs.joinmastodon.org/methods/filters/#statuses-remove) added in 4.0
  * [ ] [/api/v1/filters](https://docs.joinmastodon.org/methods/filters/#v1) all v1 filters have been deprecated in 4.0, still exist for backwards compat.
  * [ ] [POST /api/v1/reports HTTP/1.1](https://docs.joinmastodon.org/methods/reports/#post) 4.0.0 - category is now optional if rule_ids is provided, 4.2.0 - add legal category
  * [ ] [GET /api/v1/followed_tags HTTP/1.1](https://docs.joinmastodon.org/methods/followed_tags/#get) 4.0.0 - added, 4.1.0 - add pagination headers
  * [ ] [GET /api/v1/tags/:id HTTP/1.1](https://docs.joinmastodon.org/methods/tags/#get) 4.0.0 - added
  * [ ] [POST /api/v1/tags/:id/follow HTTP/1.1](https://docs.joinmastodon.org/methods/tags/#follow) 4.0.0 - added, 4.1.0 - this action is now idempotent
  * [ ] [POST /api/v1/tags/:id/unfollow HTTP/1.1](https://docs.joinmastodon.org/methods/tags/#unfollow) 4.0.0 - added
  * [ ] [DELETE /api/v1/profile/avatar HTTP/1.1](https://docs.joinmastodon.org/methods/profile/#delete-profile-avatar) 4.2.0 - added
  * [ ] [DELETE /api/v1/profile/header HTTP/1.1](https://docs.joinmastodon.org/methods/profile/#delete-profile-header) 4.2.0 - added
  * [ ] [GET /api/v1/statuses/:id/context HTTP/1.1](https://docs.joinmastodon.org/methods/statuses/#context) 4.0.0 - limit unauthenticated requests
  * [ ] [POST /api/v1/statuses/:id/translate HTTP/1.1](https://docs.joinmastodon.org/methods/statuses/#translate) 4.0.0 - added
  * [ ] [PUT /api/v1/statuses/:id HTTP/1.1](https://docs.joinmastodon.org/methods/statuses/#edit) 4.0.0 - add language
  * [ ] [POST /api/v2/media HTTP/1.1](https://docs.joinmastodon.org/methods/media/#v2) 4.0.0 - Smaller media formats (image) will be processed synchronously and return 200 instead of 202. Larger media formats (video, gifv, audio) will continue to be processed asynchronously and return 202.
  * [ ] [POST /api/v1/lists HTTP/1.1](https://docs.joinmastodon.org/methods/lists/#create) 4.2.0 - added exclusive
  * [ ] [GET /api/v1/notifications HTTP/1.1](https://docs.joinmastodon.org/methods/notifications/#get) 4.0.0 - added admin.report type, 4.1.0 - notification limit changed from 15 (max 30) to 40 (max 80)
  * [ ] [POST /api/v1/push/subscription HTTP/1.1](https://docs.joinmastodon.org/methods/push/#create) 4.0.0 - added data[alerts][admin.report]
  * [ ] [PUT /api/v1/push/subscription HTTP/1.1](https://docs.joinmastodon.org/methods/push/#update) 4.0.0 - added data[alerts][admin.report]
  * [ ] [GET /api/v2/search HTTP/1.1](https://docs.joinmastodon.org/methods/search/#v2) 4.0.0 - no longer requires a user token. Without a valid user token, you cannot use the resolve or offset parameters.
  * [ ] [GET /api/v2/instance](https://docs.joinmastodon.org/methods/instance/#v2) 4.0.0 - added
  * [ ] [GET /api/v1/instance/domain_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/instance/#domain_blocks) 4.0.0 - added
  * [ ] [GET /api/v1/instance/extended_description HTTP/1.1](https://docs.joinmastodon.org/methods/instance/#extended_description) 4.0.0 - added
  * [ ] [GET /api/v1/instance/translation_languages HTTP/1.1](https://docs.joinmastodon.org/methods/instance/#translation_languages) 4.2.0 - added
  * [ ] [GET /api/v1/instance HTTP/1.1](https://docs.joinmastodon.org/methods/instance/#v1) 4.0.0 - deprecated. added configuration[accounts].
  * [ ] [GET /api/v1/admin/accounts HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#v1) 4.0.0 - support custom roles and permissions
  * [ ] [GET /api/v2/admin/accounts HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#v2) 4.0.0 - added role_ids. Support custom roles and permissions
  * [ ] [GET /api/v1/admin/accounts/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#get-one) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/approve HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#approve) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/reject HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#reject) 4.0.0 - support custom roles and permissions
  * [ ] [DELETE /api/v1/admin/accounts/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#delete) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/action HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#action) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/enable HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#enable) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/unsilence HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#unsilence) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/unsuspend HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#unsuspend) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/accounts/:id/unsensitive HTTP/1.1](https://docs.joinmastodon.org/methods/admin/accounts/#unsensitive) 4.0.0 - support custom roles and permissions
  * [ ] [GET /api/v1/admin/canonical_email_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/canonical_email_blocks/#get) 4.0.0 - added
  * [ ] [GET /api/v1/admin/canonical_email_blocks/:id HTTP/1.1](GET /api/v1/admin/canonical_email_blocks/:id HTTP/1.1) 4.0.0 - added
  * [ ] [POST /api/v1/admin/canonical_email_blocks/test HTTP/1.1](https://docs.joinmastodon.org/methods/admin/canonical_email_blocks/#test) 4.0.0 - added
  * [ ] [POST /api/v1/admin/canonical_email_blocks HTTP/1.1](POST /api/v1/admin/canonical_email_blocks HTTP/1.1) 4.0.0 - added
  * [ ] [DELETE /api/v1/admin/canonical_email_blocks/:id HTTP/1.1](DELETE /api/v1/admin/canonical_email_blocks/:id HTTP/1.1) 4.0.0 - added
  * [ ] [POST /api/v1/admin/dimensions HTTP/1.1](https://docs.joinmastodon.org/methods/admin/dimensions/#get) 4.0.0 - support custom roles and permissions
  * [ ] [GET /api/v1/admin/domain_allows HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_allows/#get) 4.0.0 - added
  * [ ] [GET /api/v1/admin/domain_allows/:id HTTP/1.1](GET /api/v1/admin/domain_allows/:id HTTP/1.1) 4.0.0 - added
  * [ ] [POST /api/v1/admin/domain_allows HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_allows/#create) 4.0.0 - added
  * [ ] [DELETE /api/v1/admin/domain_allows/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_allows/#delete) 4.0.0 - added
  * [ ] [GET /api/v1/admin/domain_blocks HTTP/1.1](4.0.0 - added) 4.0.0 - added
  * [ ] [GET /api/v1/admin/domain_blocks/:id HTTP/1.1](GET /api/v1/admin/domain_blocks/:id HTTP/1.1) 4.0.0 - added
  * [ ] [POST /api/v1/admin/domain_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_blocks/#create) 4.0.0 - added
  * [ ] [PUT /api/v1/admin/domain_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_blocks/#update) 4.0.0 - added 
  * [ ] [DELETE /api/v1/admin/domain_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/domain_blocks/#delete) 4.0.0 - added
  * [ ] [GET /api/v1/admin/email_domain_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/email_domain_blocks/#get) 4.0.0 - added
  * [ ] [GET /api/v1/admin/email_domain_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/email_domain_blocks/#get-one) 4.1.0 - added
  * [ ] [POST /api/v1/admin/email_domain_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/email_domain_blocks/#create) 4.0.0 - added
  * [ ] [DELETE /api/v1/admin/email_domain_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/email_domain_blocks/#delete) 4.0.0 - added
  * [ ] [GET /api/v1/admin/ip_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/ip_blocks/#get) 4.0.0 - added
  * [ ] [GET /api/v1/admin/ip_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/ip_blocks/#get-one) 4.0.0 - added
  * [ ] [POST /api/v1/admin/ip_blocks HTTP/1.1](https://docs.joinmastodon.org/methods/admin/ip_blocks/#create) 4.0.0 - added
  * [ ] [PUT /api/v1/admin/ip_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/ip_blocks/#update) 4.0.0 - added
  * [ ] [DELETE /api/v1/admin/ip_blocks/:id HTTP/1.1](https://docs.joinmastodon.org/methods/admin/ip_blocks/#delete) 4.0.0 - added
  * [ ] [POST /api/v1/admin/measures HTTP/1.1](https://docs.joinmastodon.org/methods/admin/measures/#get) 4.0.0 - support custom roles and permissions
  * [ ] [/api/v1/admin/reports HTTP/1.1](https://docs.joinmastodon.org/methods/admin/reports/) 4.0.0 - support custom roles and permissions
  * [ ] [POST /api/v1/admin/retention HTTP/1.1](https://docs.joinmastodon.org/methods/admin/retention/#create) 4.0.0 - support custom roles and permissions
  * [ ] [GET /api/v1/admin/trends/tags HTTP/1.1](GET /api/v1/admin/trends/tags HTTP/1.1) 4.0.0 - Returns an array of Tag due to a bug, 4.1.0 - Bug fixed
=======
>>>>>>> parent of bc03077 (adding endpoints to TODO that need updating)

General improvements that would be good to do before doing another release
--------------------------------------------------------------------------
* [x] Split mastodon.py into parts in some way that makes sense, it's getting very unwieldy
* [x] Fix the CI (forever task)
* [ ] Get test coverage like, real high
* [x] Add all those streaming events??
* [x] Document return values (skipping this for a bit to then do it at the end with tooling)
    * [x] Do this with models properly, that would be cool as heck
* [x] Add links to mastodon docs to entities and endpoints
* [ ] Also add links to tests to the docstrings so people can see usage examples