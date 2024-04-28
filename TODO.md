API relevant changes since last release / "to implement" list:

Refer to mastodon changelog and API docs for details when implementing, add or modify tests where needed

4.0.0 and beyond
----------------
* [ ] Document all the endpoints we need to add
  * [ ] /api/v1/accounts/:id/followers was changed in 4.0
  * [ ] /api/v1/accounts/:id/following was changed in 4.0
  * [ ] /api/v1/accounts/:id/follow was changed in 4.0, added languages
  * [ ] /api/v1/accounts/:id/pin changed in 4.0, now idempotent
  * [ ] /api/v1/accounts/relationships changed in 4.0, added with_suspend param
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
