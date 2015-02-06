## Contributing to this repository

This repository is a part of our PCI-compliant CDE (Cardholder Data Environment).
This means that there are certain guidelines which need to be followed:

* All associated tickets must be marked as change type `Substantial` or higher.
* All pull requests must have the secure coding checklistcompleted (either in the description of the ticket or in a comment).
* All associated tickets must have been approved by a majority of the [Wave CAB](https://waveaccounting.atlassian.net/wiki/pages/viewpage.action?pageId=55083505) (Change Advisory Board).

### Secure coding checklist

```
### Secure coding checklist

* [ ] No raw SQL executes untrusted, unsanitized or unvalidated parameters.
* [ ] Session variable is not present on the URL.
* [ ] Passwords are using an adaptive hashing algorithm.
* [ ] Code is free from XSS exploits.
* [ ] URL parameters are constrained to the logged in user.
* [ ] Administrative functionality is only provided to Wave authorized users.
* [ ] Ensure information is exposed only to authorized users.
* [ ] URLs are protected by backend authorization, rather than hiding in the front-end.
* [ ] Dynamic URL-based redirects are validated either against a white-list on the backend, mapped to a token on the backend, or reference relative url paths.
* [ ] Ensure we do not incur > O(n+1) queries when dealing with collections of data.
* [ ] Ensure any libraries are pinned to the expected version.
```
