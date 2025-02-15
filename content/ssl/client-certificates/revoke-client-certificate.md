---
pcx_content_type: how-to
title: Revoke a client certificate
weight: 8
---

# Revoke a client certificate

You can revoke a client certificate you previously generated with the default [Cloudflare Managed CA](/ssl/client-certificates/).

It is not possible to permanently delete client certificates generated with the default Cloudflare Managed CA. Once revoked, these client certificates will still be listed in **SSL/TLS > Client Certificates**, and can be restored at any time.

## Steps

1.  Log in to the [Cloudflare dashboard](https://dash.cloudflare.com) and select your account and application.
2.  Go to **SSL** > **Client Certificates**.
3.  Select the certificate you want to revoke.
4.  Select **Revoke** and confirm the operation.

{{<Aside type="warning" header="Important">}}

After revoking a certificate, you must update any mTLS rules that check for the presence of a client certificate so that they block all requests that include a revoked certificate.

For more information, refer to [Check for revoked certificates](/api-shield/security/mtls/configure/#check-for-revoked-certificates).

{{</Aside>}}
