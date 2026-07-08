---
share: true
created: 2023-10-30T14:29
updated: 2026-07-08T15:32
---
Nguồn:: [GitHub - mblais/fibery-script-management: Remote script management for Fibery.io automations](https://github.com/mblais/fibery-script-management)
[Sự khác biệt giữa IDE và trình soạn thảo văn bản nằm ở việc compile code. Nên chính xác mà nói thì không có IDE để viết JS cho máy khách](../../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/Kh%C3%A1i%20ni%E1%BB%87m%20c%C6%A1%20b%E1%BA%A3n/IDE/S%E1%BB%B1%20kh%C3%A1c%20bi%E1%BB%87t%20gi%E1%BB%AFa%20IDE%20v%C3%A0%20tr%C3%ACnh%20so%E1%BA%A1n%20th%E1%BA%A3o%20v%C4%83n%20b%E1%BA%A3n%20n%E1%BA%B1m%20%E1%BB%9F%20vi%E1%BB%87c%20compile%20code.%20N%C3%AAn%20ch%C3%ADnh%20x%C3%A1c%20m%C3%A0%20n%C3%B3i%20th%C3%AC%20kh%C3%B4ng%20c%C3%B3%20IDE%20%C4%91%E1%BB%83%20vi%E1%BA%BFt%20JS%20cho%20m%C3%A1y%20kh%C3%A1ch.md)

Nếu url có ký tự unicode thì cần unescape nó:
```PowerShell
node --env-file=.env .\fibscripts.js pull --url=https://quacau.fibery.io/fibery/space/Định_kỳ_đóng_phí/database/Hợp_đồng/automations/rule/6799ad300d3901c00626d49e/actions
```
Nguồn:: [No script is pulled even when the url is correct · Issue #2 · mblais/fibery-script-management](https://github.com/mblais/fibery-script-management/issues/2)
Nơi thảo luận: [Beta testers wanted for Fibery script management tool - API & Programming - Fibery Community](https://community.fibery.io/t/beta-testers-wanted-for-fibery-script-management-tool/5466/14)
