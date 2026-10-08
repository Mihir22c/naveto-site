# naveto-site

Naveto's website, served by GitHub Pages at <https://naveto.mihirbavisi.com/>.

| Path | Page |
|---|---|
| `/` | Home page |
| `/privacy/` | Privacy policy (linked from both store listings and the app) |
| `/delete-account/` | Account deletion steps (Play Console → Data safety → Delete account URL) |

**Do not edit anything here.** The source is in the app repository
(`GermanVocabCards/docs/site/`, `docs/privacy-policy.html`,
`docs/delete-account.html`), where the app's tests check it, and the numbers
on the home page are read from the app's content when the site is built.
Change it there, then:

```sh
python3 pipeline/build_site.py      # from the app repository root
cd naveto-site && git add -A && git commit -m "Update site" && git push
```

Pages settings: Source = Deploy from a branch, `main`, `/ (root)`; Custom
domain = `naveto.mihirbavisi.com` (the `CNAME` file here keeps it); Enforce HTTPS on.
DNS: `CNAME naveto -> mihir22c.github.io`.
