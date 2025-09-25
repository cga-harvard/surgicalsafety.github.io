# surgicalsafety.github.io
## Repository for redirects for surgicalsafety.cga.harvard.edu
### General Instructions
[https://docs.github.com/en/pages/quickstart](https://docs.github.com/en/pages/quickstart)

### Redirecting surgicalsafety.cga.harvard.edu
1.  Follow the directions here to verify the github pages domain for the cga-harvard organization:  https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages#verifying-a-domain-for-your-organization-site

Note that when creating the text record in the DNS, you will need to enter the FQDN (Fully Qualified Domain Name) rather than just the host name.  If the text record is
```
_github-pages-challenge-cga-harvard.surgicalsafety.cga
```
you must enter
```
_github-pages-challenge-cga-harvard.surgicalsafety.cga.harvard.edu
```
in the DNS.

1.  Create a repository named surgicalsafety.github.io  The repository name must end in github.io

1.  Create a file called `CNAME` with the contents
```
surgicalsafety.cga.harvard.edu
```


1.  Place this file in the top level directory:
```
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="refresh" content="0; url=https://gis.harvard.edu/surgical-safety-web-map/" />
    <title>Redirecting…</title>
    <link rel="canonical" href="https://gis.harvard.edu/surgical-safety-web-map/" />
  </head>
  <body>
    <p>If you are not redirected, <a href="https://gis.harvard.edu/surgical-safety-web-map/">click here</a>.</p>
  </body>
</html>
```

1.  Go to your repo’s `Settings > Pages`.  Under "Branch" use the first dropdown to choose "main", then click "Save."

1.  Set your DNS CNAME in the HUIT DNS for `surgicalsafety.cga.harvard.edu` to point to `cga-harvard.github.io`  This has to be done before configuring your custom domain.

1.  Under “Custom domain”, enter `surgicalsafety.cga.harvard.edu` and save.

1.  Enable `Enforce HTTPS` once the custom domain is recognized.
