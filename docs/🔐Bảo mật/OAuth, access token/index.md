---
share: true
created: 2023-10-30T14:29
updated: 2025-11-16T09:07
title: OAuth, access token
---
## Google API
Thứ được tải về bằng tay
```json
{
  "installed": {
    "client_id": Để authorization server biết đây là client nào,
    "project_id": "gtm-pjx4b43k-n2jmm",
    "auth_uri": "https://accounts.google.com/o/oauth2/auth",
    "token_uri": "https://oauth2.googleapis.com/token",
    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
    "client_secret": Để authorization server đảm bảo rằng clien này chính là client đó,
    "redirect_uris": [
      "http://localhost"
    ]
  }
}
```
[Client ID là để máy cấp quyền biết client nào là client nào, còn client secret là để nó đảm bảo rằng client này chính là client đó](./X%C3%A1c%20th%E1%BB%B1c,%20c%E1%BA%A5p%20ph%C3%A9p/Client%20ID%20l%C3%A0%20%C4%91%E1%BB%83%20m%C3%A1y%20c%E1%BA%A5p%20quy%E1%BB%81n%20bi%E1%BA%BFt%20client%20n%C3%A0o%20l%C3%A0%20client%20n%C3%A0o,%20c%C3%B2n%20client%20secret%20l%C3%A0%20%C4%91%E1%BB%83%20n%C3%B3%20%C4%91%E1%BA%A3m%20b%E1%BA%A3o%20r%E1%BA%B1ng%20client%20n%C3%A0y%20ch%C3%ADnh%20l%C3%A0%20client%20%C4%91%C3%B3.md)

Thứ được tạo ra khi đã xác thực:
```json
{
  "type": "authorized_user",
  "client_id": Để authorization server biết đây là client nào,
  "client_secret": Để authorization server đảm bảo rằng clien này chính là client đó,
  "refresh_token": 
}
```