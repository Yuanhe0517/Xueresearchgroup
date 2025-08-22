---
# Leave the homepage title empty to use the site title
title: Xue
date: 2022-10-24
type: landing

sections:
  - block: markdown
    content:
      title: |
         Soft Mechanics Lab (SML)
      image:
        filename: 
      text: |
        <div align="justify">
        Soft matter includes synthetic materials (e.g., liquid crystals, gels) and living systems such as cells and tissues. Characterized by “weak stimuli, strong responses,” it shows highly nonlinear deformation under external loads. Such behaviors play key roles in diseases (e.g., cancer) and life processes (e.g., embryonic development). The Soft Mechanics Lab (SML) focuses on the mechanics of soft materials and tissues, with emphasis on the following areas:
        <div> 

  - block: slider
    content:
      slides:
        - title: "Mechanics of soft materials"
          content: |
    
          align: center
          background:
            image:
              filename: tissue.jpg
              filters:
                brightness: 0.7
            position: center
            color: '#666'
          link:
            icon: book
            icon_pack: fas
            text: Read more
            url: "/research/soft-material/"  # 将链接指向具体研究的详情页面

        - title: "Mechanics of soft tissues"
          content: |
  
          align: left
          background:
            image:
              filename: tissue.jpg
              filters:
                brightness: 0.7
            position: center
            color: '#555'
          link:
            icon: book
            icon_pack: fas
            text: Read more
            url: "/research/soft-tissue/"  # 详情页面链接

        - title: "Mechanics of "
          content: |
            Investigating how invasive tumors generate mechanical stresses that affect surrounding tissue and influence tumor progression and metastasis.
          align: right
          background:
            image:
              filename: contact.jpg
              filters:
                brightness: 0.5
            position: center
            color: '#333'
          link:
            icon: book
            icon_pack: fas
            text: Read more
            url: "https://example.com/research/tumor-growth"  # 详情页面链接

    design:
      is_fullscreen: true          # 3) 或者用下一行强制高度（二选一即可）
      # slide_height: '420px'
      loop: false
      interval: 3000

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
---
