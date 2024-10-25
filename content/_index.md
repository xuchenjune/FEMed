---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Few Exemplar-Based General Medical Image Segmentation via Domain-Aware Selective Adaptation
      image:
        filename: umap.png #results2.jpg
      text: |
        
        
        The research proposes a domain-aware selective adaptation method for medical image segmentation using fewer exemplars.This approach adapts general knowledge from large natural image models to medical domains, overcoming limitations in existing methods and offering an efficient, LMIC-friendly solution for healthcare diagnostics.
        <br/>
        The dimensionality reduction visualisation map shows the relative relationship and distribution of different data sets in a two-dimensional feature space. It can be seen the characteristics of the medical data set (red points) compared to the general natural data set (blue/black points). A clear domain gap can be observed from this visualisation.
  
  # - block: collection
  #   content:
  #     title: Latest News
  #     subtitle:
  #     text:
  #     count: 5
  #     filters:
  #       author: ''
  #       category: ''
  #       exclude_featured: false
  #       publication_type: ''
  #       tag: ''
  #     offset: 0
  #     order: desc
  #     page_type: post
  #   design:
  #     view: card
  #     columns: '1'
  # 
  - block: markdown
    content:
      title: <a href="https://mix.jianbojiao.com/people/">Chen Xu&dagger;</a>, <a href="https://mix.jianbojiao.com/people/">Qiming Huang&dagger;</a>, <a href="https://mix.jianbojiao.com/people/">Yuqi Hou</a>, Jiangxing Wu, Fan Zhang, <a href="https://cvlab-uob.github.io/">Hyung Jin Chang</a>, <a href="https://jianbojiao.com/">Jianbo Jiao</a> 
      subtitle: <a href="https://accv2024.org/">The MIx Group</a>, University of Birmingham, Fudan University
      text: |
        <div style="text-align: center;margin:-20px 0px 10px 0px"><a href="https://accv2024.org/">The Springer: Asian Conference on Computer Vision (ACCV) 2024</a></div>
        {{< button-group >}}
          {{% cta cta_link="/FEMedSegment.pdf" cta_text=" Paper " %}}
          {{% cta cta_link="https://arxiv.org/abs/2410.09254" cta_text=" arXiv " %}}
          {{% cta cta_link="https://github.com/xuchenjune/FEMedSegment" cta_text="Code" %}}
          {{% cta cta_link="https://mix.jianbojiao.com/" cta_text="Group" %}}
        {{< /button-group >}}
    design:
      columns: '1'

  - block: markdown
    content:
      title: 
      subtitle: ''
      text: |
        <div class="code-container" style="text-align: center; margin-top: -100px;">
            <div class="code-text" style="font-weight: bold;font-size: 24px;">Main Contributions: </div>
            <div class="code-text"></div>
        </div>
        <div class="code-container" style="">
            <div class="line-number">1. </div>
            <div class="code-text">We propose, to our knowledge, the first attempt towards adapting a general prior knowledge to various medical domains with only a few exemplars.</div>
        </div>
        <div class="code-container">
            <div class="line-number">2. </div>
            <div class="code-text">We introduce a new domain-aware selective adaptation approach, which enables simple yet effective fine-tuning of large pre-trained models and boosts their performance in target domains.</div>
        </div>
        <div class="code-container">
            <div class="line-number">3. </div>
            <div class="code-text">We identify the issues with the use of prompts in current prompt-based medical image segmentation models and propose a coarse prompt setting that better aligns with real-world scenarios.</div>
        </div>
        <div class="code-container">
            <div class="line-number">4. </div>
            <div class="code-text">Extensive experiments validate the effectiveness of the proposed method, achieving state-of-the-art performance under the challenging few exemplar setting, surpassing existing works by a large margin.</div>
        </div>
    design:
      columns: '1'
  
  - block: markdown
    content:
      title: 
      subtitle: ''
      text: |
        <div style="text-align: center; margin-top: -100px;">
          <div>
            <img src="images/net.png" alt="Author 1" style="width: 100%; />
            <a style="text-align: center;" href="https://example.com/author1" style="font-size: 32">FEMed Architecture</a>
            <p style="text-align: left;">The architecture of our Image Encoder enhanced with two specialized Adapters: (a) the Multi-Scale Features Adapter that captures features at various granularities through pyramid pooling, and (b) the High-Frequency Adapter that emphasizes salient textural details from frequency domain analysis. (c) These Adapters feed into the Selection Module, which uses a trainable binary decision layer to selectively integrate the most informative feature set at each transformer stage, effectively tailoring the feature landscape for optimal tumour delineation in CT/MRI scans.
            </p>
          </div>
        </div>
    design:
      columns: '1'

  - block: markdown
    content:
      title: 
      subtitle: ''
      text: |
        <div class="code-container" style="text-align: center; margin-top: -100px;">
            <div class="code-text" style="font-weight: bold;font-size: 24px;">Visual Prompt Settings: </div>
            <div class="code-text"></div>
        </div>
        <div class="code-container">
            <div class="code-text">The segment anything model (SAM) can adopt many types of visual prompts, \ie, scribbles, clicks, or boxes to segment the arbitrary object within the image. It demonstrates highly generalized segmentation performance using prompts during training and testing. This paper focuses on the form of bounding box prompt. Consequently, mainstream approaches to applying SAM for medical image segmentation follow this setting, utilizing prompts in both training and testing. We highlight that the previous methods' use of prompts in the medical segmentation domain is not suitable. We categorize prompts into two types: \textbf{fine-grained prompts and coarse prompts}. The fine-grained prompts, as shown in Fig. \ref{compa} A and C, are customary user-provided or generated from manually annotated results. They are bespoke for each image and provide strong prior knowledge of the target location. Coarse prompts, as illustrated in Figures B and D, remain consistent across different images and offer almost no prior knowledge. Note that our definitions of fine-grained and coarse prompts differ from those in <sup><a href="#ref1">[1]</a></sup>.</div>
            <div class="code-text"></div>
        </div>
        <br>
        <div class="code-container">
            <div class="line-number">Setting A: </div>
            <div class="code-text">Trained with file-grained bbox prompts and tested with fine-grained bbox prompts.</div>
        </div>
        <div class="code-container">
            <div class="line-number">Setting B: </div>
            <div class="code-text">Trained with file-grained bbox prompts and tested with coarse bbox prompts.</div>
        </div>
        <div class="code-container">
            <div class="line-number">Setting C: </div>
            <div class="code-text">Trained with coarse bbox prompts and tested with fine-grained bbox prompts.</div>
        </div>
        <div class="code-container">
            <div class="line-number">Setting D: </div>
            <div class="code-text">Trained with coarse bbox prompts and tested with coarse bbox prompts.</div>
        </div>
        <br>
        <div class="code-container">
            <div class="code-text">Most SAM adapters in medical image segmentation rely on user-provided prompts or assuming prompts generated from segmentation annotations, i.e., the lesion area is already known, and a bounding box prompt for the lesion area is given, expecting the model to accurately segment the lesion within this region (setting A). However, this assumption is not applicable in real diagnostic scenarios. For unseen samples, the lesion area is unknown, making it impossible to provide such fine-grained visual prompts. Therefore, a prompt setting that aligns with real-world applications should be settings B and D, where only a coarse bounding box prompt can be provided during inference, for example, a rectangular box almost the same size as the original image. Since setting B uses different prompts for training and testing, performance is affected. Thus, this paper primarily investigates setting D in Fig. \ref{compa}. It's more challenging compare to the other settings since these is no accurate lesion area information provided. </div>
            <div class="code-text"></div>
        </div>
        <ol style="margin-top:20px;font-size: 12">
            <li id="ref1" style="font-size: 12">Yang, Lingfeng, Wang, Yueze, Li, Xiang, Wang, Xinlong, Yang, Jian. <a href="https://arxiv.org/abs/2306.04356">"Fine-grained visual prompting."</a> <i>Advances in Neural Information Processing Systems</i>, vol. 36, 2024.</li>
        </ol>
        
    design:
      columns: '1'
      
  - block: markdown
    content:
      title:
      subtitle: ''
      text: |
        <div style="text-align: center;">
          <div>
            <img src="images/compa.jpg" alt="Author 1" style="width: 100%;/>
            <a style="text-align: center;" href="https://example.com/author1" >Prompt Strategy</a>
            <p style="text-align: left;">Four settings of using bbox prompts during training and testing stages. The coarse bounding box prompt is designed to be almost the same size as the input image data, with different ratios indicating the proportion of pixels by which the rectangle is shrunk inward relative to the entire image. A pseudo-code for coarse bbox prompt generation is shown in Algorithm 1 in the paper.</p>
          </div>
        </div>

  - block: hero
    content:
      title: 
      image:
        filename: results2.jpg
      text: |
        Comparison from MedSAM<sup><a href="#ref2">[2]</a></sup>, SAM-MED2D<sup><a href="#ref3">[3]</a></sup>, and our FEMed method (5-shot, 10-shot). The first column is the input image, the second column is the image with coloured ground truth masks, and the third and fourth columns are the image with coloured predicted masks by MedSAM and SAM-MED2D. The right two columns are the image with coloured predicted masks by our FEMed method.

        <ol>
            <li id="ref2">Ma, et al. "Segment Anything in Medical Images with MedSAM." <i>2024</i>.</li>
            <li id="ref3">Cheng, et al. "SAM-MED2D: Medical Image Segmentation with Segment Anything Model." <i>2023</i>.</li>
        </ol>

  - block: collection
    content:
      title: Latest Preprints
      text: ""
      count: 5
      filters:
        folders:
          - publication
        publication_type: 'article'
    design:
      view: citation
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="https://mix.jianbojiao.com/" cta_text="Meet the team →" %}}
    design:
      columns: '1'

  - block: markdown
    content:
      title: "Our Authors"
      text: |
        <div class="author-group">
          <div class="author-item">
            <img src="images/chenxu.jpg" alt="Author 1" class="author-photo"/>
            <a href="https://example.com/author1" class="author-name">Chen Xu</a>
          </div>
          <div class="author-item">
            <img src="images/Qiming.jpg" alt="Author 2" class="author-photo"/>
            <a href="https://example.com/author2" class="author-name">Qiming Huang</a>
          </div>
          <div class="author-item">
            <img src="images/yuqi.jpg" alt="Author 3" class="author-photo"/>
            <a href="https://example.com/author3" class="author-name">Yuqi Hou</a>
          </div>
          <!-- 继续添加其他作者 -->
          <div class="author-item">
            <img src="images/hyungjin.jpg" alt="Author 4" class="author-photo"/>
            <a href="https://example.com/author3" class="author-name">Hyung Jin Chang</a>
          </div>
          <div class="author-item">
            <img src="images/jiao-jianbo.jpg" alt="Author 5" class="author-photo"/>
            <a href="https://example.com/author3" class="author-name">Jianbo Jiao</a>
          </div>
        </div>
    design:
      columns: '1'
---
