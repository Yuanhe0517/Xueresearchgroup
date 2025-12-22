---
# Leave the homepage title empty to use the site title
title: Xue
date: 2022-10-24
type: landing

sections:
  # ─────────────────────────────────────────────────────────
  # 顶部：大标题 + 引导段落（p1 风格）+ 全局样式与字体大小控制
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      title: |
        Soft Mechanics Lab (SML)
      text: |
        Soft matter encompasses a broad class of materials—from synthetic systems like liquid crystals and polymers to living matter such as cells and biological tissues. A defining characteristic of soft matter is its capacity for large deformations and pronounced mechanical responses under external stimuli. This property is central not only to material science but also to biology, where fundamental processes like embryonic development and pathologies such as cancer involve large-scale tissue flow, deformation, and three-dimensional morphogenesis. At the Soft Mechanics Lab, we integrate theoretical modeling, numerical simulations, and quantitative experiments to uncover the morpho-mechanics of soft matter. Our research focuses on two interrelated frontiers:

        1. Morphogenesis of biological tissues: how tissue shape is sculpted via mechanochemical coupling, stress-modulated growth and remodeling, nematic order and topological defects.
        2. Pattern formation of soft materials: how soft materials and elastic structures spontaneously form regular and irregular surface patterns via elastic instability, phase transition and multi-physical coupling mechanisms.

        Our research seeks to decipher the mechanobiological principles that guide tissue development and regeneration. This knowledge is pivotal for engineering next-generation biological constructs and inspiring novel, life-like actuators for soft robotics.

        <!-- ====== 页面样式（含字体大小总控） ====== -->
        <style>
          /* —— 字体大小总控：改这些变量即可 —— */
          :root{
            --home-h1: clamp(24px, 3.3vw, 44px);   /* 顶部大标题 */
            --home-h2: clamp(28px, 3.2vw, 34px); /* 每个模块标题 */
            --home-text: 1.05rem;                /* 段落/列表字号 */
            --home-btn: 0.7rem;                    /* 按钮字号 */
            --home-lh: 1.65;                     /* 行距 */
          }
          /* 顶部区块标题/正文（兼容不同主题结构） */
          .wg-markdown:first-of-type .section-heading h1,
          .wg-markdown:first-of-type .section-heading h2,
          .wg-markdown:first-of-type h1{
            font-size: var(--home-h1);
          }
          .wg-markdown:first-of-type p,
          .wg-markdown:first-of-type li{
            font-size: var(--home-text);
            line-height: var(--home-lh);
            text-align: justify;
          }
          .wg-markdown:first-of-type p{ margin: 0 0 1rem; }
          .wg-markdown:first-of-type ol{ margin: 0.25rem 0 1rem 1.2rem; }

          /* 左文右图两栏布局 */
          .area { display:grid; grid-template-columns:minmax(0,1.1fr) minmax(0,1.5fr); gap:24px; align-items:center; }
          .area h2{ margin:.2rem 0 .6rem; font-size: var(--home-h2); }
          .area p, .area li{ font-size: var(--home-text); line-height: var(--home-lh); }
          .area ul{ margin:.4rem 0 0 1.2rem; }
          .imggrid { display:grid; grid-template-columns:1fr 1fr; gap:12px; }
          .imggrid > img:only-child{ grid-column: 1 / -1; } /* 单张图时横跨两列 */
          .imggrid > img:nth-child(3){ grid-column:1 / -1; } /* 第三张图横跨两列 */
          .imgcell{ grid-column: 1 / -1; }
          .imgcap{ margin-top:8px; font-size:.92rem; line-height:1.25; color:#555; text-align:center; }
          .btn-link{ display:inline-block; padding:.15rem .9rem; border-radius:10px; border:1px solid currentColor; text-decoration:none; transition:all .15s ease; font-size: var(--home-btn); }
          @media (max-width: 900px){
            .area{ grid-template-columns:1fr; }
            .imggrid{ grid-template-columns:1fr; }
          }

          /* 三个模块主题色 */
          .brand-1{ --brand:#2B6FAE; }   /* p1 蓝 */
          .brand-2{ --brand:#9E3B7A; }   /* p2 紫红 */
          .brand-3{ --brand:#EE8A2E; }   /* p3 橙   */

          .area.brand-1 h2, .area.brand-2 h2, .area.brand-3 h2 { color: var(--brand); }
          .area.brand-1 .btn-link, .area.brand-2 .btn-link, .area.brand-3 .btn-link { color: var(--brand); border-color: var(--brand); }
          .area.brand-1 .btn-link:hover, .area.brand-2 .btn-link:hover, .area.brand-3 .btn-link:hover { background: var(--brand); color:#fff; }
        </style>
    design:
      columns: '1'

  # ─────────────────────────────────────────────────────────
  # 模块 1（蓝色）
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <div class="area brand-1">
          <div>
            <h2>Morphogenesis of biological tissues</h2>
            <ul>
              <li>Mechanochemical coupling</li>
              <li>Stress-modulated growth and remodeling</li>
              <li>Nematic order and topological defects</li>
            </ul>
          </div>
          <div class="imggrid">
            <div class="imgcell">
              <img src="/images/research/morpho_1.png" alt="Mechanics example 1" loading="lazy" style="width:100%;height:auto;border-radius:12px;object-fit:cover;">
              <div class="imgcap">Mechano-chemical bistability for crypt morphogenesis</div>
            </div>
          </div>
        </div>
    design:
      columns: '1'

  # ─────────────────────────────────────────────────────────
  # 模块 2（紫红）
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <div class="area brand-2">
          <div>
            <h2>Pattern formation of soft materials</h2>
            <ul>
              <li>Elastic instability</li>
              <li>Phase transition</li>
              <li>Multi-physical coupling mechanisms </li>
            </ul>
          </div>
          <div class="imggrid">
            <div class="imgcell">
              <img src="/images/research/morpho_2.png" alt="Morphogenesis example 1" loading="lazy" style="width:100%;height:auto;border-radius:12px;object-fit:cover;">
              <div class="imgcap">‘Snap-through’ instabilities in a simple elastic system</div>
            </div>
          </div>
        </div>
    design:
      columns: '1'

  # # ─────────────────────────────────────────────────────────
  # # 模块 3（橙色）
  # # ─────────────────────────────────────────────────────────
  # - block: markdown
  #   content:
  #     text: |
  #       <div class="area brand-3">
  #         <div>
  #           <h2>Bionics of soft tissue </h2>
  #           <ul>
  #             <li>soft devices</li>
  #           </ul>
  #           <p><a class="btn-link" href="/research/">Read more →</a></p>
  #         </div>
  #         <div class="imggrid">
  #           <img src="/images/research/protein_1.jpg" alt="Bionics" loading="lazy" style="width:100%;height:auto;border-radius:12px;object-fit:cover;">

  #         </div>
  #       </div>
  #   design:
  #     columns: '1'

  # ─────────────────────────────────────────────────────────
  # 底部 CTA
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        {{% cta cta_link="/people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
---
---
