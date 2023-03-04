---
<%-*
    let title = tp.file.title;
        if (title.startsWith("Untitled")) {
            let titleInput = await tp.system.prompt("Title");
            
            if (titleInput != null) {
                title = titleInput;
                await tp.file.rename(`${title}`);
            }
    }
%>
title: "<%* tR += title %>"
date: "<% tp.date.now('YYYY-MM-DD HH:mm:ss') %>"
publish: true
slug: "<% tp.file.cursor() %>"
tags: []
---

Contents here