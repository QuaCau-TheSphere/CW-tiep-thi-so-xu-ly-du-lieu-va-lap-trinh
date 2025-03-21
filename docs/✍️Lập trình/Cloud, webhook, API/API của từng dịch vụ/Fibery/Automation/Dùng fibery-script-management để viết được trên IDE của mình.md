---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
Nguồn:: [GitHub - mblais/fibery-script-management: Remote script management for Fibery.io automations](https://github.com/mblais/fibery-script-management)
[VS Code chỉ là code editor, không phải IDE](../../../../C%C3%B4ng%20c%E1%BB%A5/IDE%20(VS%20Code)/VS%20Code%20ch%E1%BB%89%20l%C3%A0%20code%20editor,%20kh%C3%B4ng%20ph%E1%BA%A3i%20IDE.md)

Nếu url có ký tự unicode thì cần unescape nó:
```PowerShell
node --env-file=.env .\fibscripts.js pull --url=https://quacau.fibery.io/fibery/space/Định_kỳ_đóng_phí/database/Hợp_đồng/automations/rule/6799ad300d3901c00626d49e/actions
```
Nguồn:: [No script is pulled even when the url is correct · Issue #2 · mblais/fibery-script-management](https://github.com/mblais/fibery-script-management/issues/2)
Nơi thảo luận: [Beta testers wanted for Fibery script management tool - API & Programming - Fibery Community](https://community.fibery.io/t/beta-testers-wanted-for-fibery-script-management-tool/5466/14)