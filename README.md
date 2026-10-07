# naveto-site

The public pages for the Naveto app, served by GitHub Pages at
<https://naveto.mihirbavisi.com/>.

| Path | Page |
|---|---|
| `/` | Privacy policy (linked from both store listings and the app) |
| `/delete-account/` | Account deletion steps (Play Console → Data safety → Delete account URL) |

**Do not edit the HTML here.** The source is in the app repository
(`GermanVocabCards/docs/privacy-policy.html` and `docs/delete-account.html`),
where the app's tests check it. Change it there, then:

```sh
python3 pipeline/build_site.py      # from the app repository root
cd naveto-site && git add -A && git commit -m "Update policy" && git push
```

Pages settings: Source = Deploy from a branch, `main`, `/ (root)`; Custom
domain = `naveto.mihirbavisi.com` (the `CNAME` file here keeps it); Enforce HTTPS on.
DNS: `CNAME naveto -> mihir22c.github.io`.
