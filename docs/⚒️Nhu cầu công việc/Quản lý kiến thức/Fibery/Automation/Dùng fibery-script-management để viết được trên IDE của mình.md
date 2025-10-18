---
share: true
created: 2023-10-30T14:29
updated: 2025-08-06T21:39
---
Nguồn:: [GitHub - mblais/fibery-script-management: Remote script management for Fibery.io automations](https://github.com/mblais/fibery-script-management)
[Do IDE là để compile code, nên chính xác mà nói thì không có IDE cho JS](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/C%C3%B4ng%20c%E1%BB%A5/IDE/Do%20IDE%20l%C3%A0%20%C4%91%E1%BB%83%20compile%20code,%20n%C3%AAn%20ch%C3%ADnh%20x%C3%A1c%20m%C3%A0%20n%C3%B3i%20th%C3%AC%20kh%C3%B4ng%20c%C3%B3%20IDE%20cho%20JS.md)

Nếu url có ký tự unicode thì cần unescape nó:
```PowerShell
node --env-file=.env .\fibscripts.js pull --url=https://quacau.fibery.io/fibery/space/Định_kỳ_đóng_phí/database/Hợp_đồng/automations/rule/6799ad300d3901c00626d49e/actions
```
Nguồn:: [No script is pulled even when the url is correct · Issue #2 · mblais/fibery-script-management](https://github.com/mblais/fibery-script-management/issues/2)
Nơi thảo luận: [Beta testers wanted for Fibery script management tool - API & Programming - Fibery Community](https://community.fibery.io/t/beta-testers-wanted-for-fibery-script-management-tool/5466/14)