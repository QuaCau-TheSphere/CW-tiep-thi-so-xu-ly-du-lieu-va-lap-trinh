---
share: true
created: 2023-10-24T18:26
updated: 2024-01-28T17:36
---

[Google tag, global site tag, gtag là những cái tên khác nhau cho đoạn script theo dõi người dùng của Google Analytics](./Google%20tag,%20global%20site%20tag,%20gtag%20l%C3%A0%20nh%E1%BB%AFng%20c%C3%A1i%20t%C3%AAn%20kh%C3%A1c%20nhau%20cho%20%C4%91o%E1%BA%A1n%20script%20theo%20d%C3%B5i%20ng%C6%B0%E1%BB%9Di%20d%C3%B9ng%20c%E1%BB%A7a%20Google%20Analytics.md), còn [Google Tag Manager là một trình quản lý các mã JavaScript được gắn vào web](./Google%20Tag%20Manager/Google%20Tag%20Manager%20l%C3%A0%20m%E1%BB%99t%20tr%C3%ACnh%20qu%E1%BA%A3n%20l%C3%BD%20c%C3%A1c%20m%C3%A3%20JavaScript%20%C4%91%C6%B0%E1%BB%A3c%20g%E1%BA%AFn%20v%C3%A0o%20web.md). Ngoài Google tag ra còn có Facebook tag, LinkedIn tag, v.v.

![](https://www.analyticsmania.com/wp-content/uploads/2022/01/image-2022-01-06T152832.289.jpg) 
Nguồn:: [GTAG vs Google Tag Manager. What is the Difference? What to Choose?](https://www.analyticsmania.com/post/gtag-vs-google-tag-manager/)

# Lợi ích của Google Tag Manager 
- The ability to deploy and modify both Google and 3rd party tags
- The ability to deploy and modify tags for both web and mobile apps
- The ability to deploy and modify tags on the fly from a web interface
- Collaboration and versioning capabilities

Nguồn:: [Google Support](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Google%20Support.md), [Tag Manager and the Google tag (gtag.js) - Tag Manager Help](https://support.google.com/tagmanager/answer/7582054?sjid=14081765469960323685-AP)

You should only use either the Google tag or Tag Manager, not both. Using both methods will have unintended consequences, such as overcounting data from your website. If you've installed both the Tag Manager snippets and the Google tag snippet, remove the snippets for one of these implementation options.
Nguồn:: [Google Support](../../../%E2%9C%8D%EF%B8%8FL%E1%BA%ADp%20tr%C3%ACnh/%CE%9E%20Ngu%E1%BB%93n%20v%C3%A0%20t%C3%A0i%20nguy%C3%AAn%20h%E1%BB%97%20tr%E1%BB%A3/%CE%9E%20Ngu%E1%BB%93n/Google%20Support.md), [[GA4] Troubleshoot tag setup on your website - Analytics Help](https://support.google.com/analytics/answer/9311124?hl=en&sjid=12272186081024095110-AP#zippy&zippy=%2Cthe-tag-manager-and-google-tag-snippets-are-both-installed%2Cthe-tag-manager-changes-have-not-been-published%2Cthe-google-tag-snippet-is-in-the-wrong-place%2Cthe-google-tag-contains-extra-whitespaces-or-characters%2Cthe-ga-configuration-tag-has-not-been-configured%2Cthe-ga-configuration-tag-does-not-have-a-trigger-condition)