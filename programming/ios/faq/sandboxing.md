---
layout: default-layout
title: DCV FAQs - Dynamsoft Capture Vision iOS Edition
description: The FAQs of Dynamsoft Capture Vision iOS edition.
keywords: FAQs, index, iOS
needAutoGenerateSidebar: true
noTitleIndex: false
---

# How to deal with "Sandbox: rsync.sambe(10288)..." error

If you meet an error like this:

<div align="center">
   <p><img src="../../../assets/img/sandboxing.png" alt="sandboxing" width="50%" /></p>
   <p>Sandboxing error</p>
</div>

Find "User Script Sandboxing" setting in the **Build Settings/Build Options** of your project and change it to "No".
