# Section 1: Problem & User ≤ 200 words
## Target users
  
  Undergraduate students, graduate students, PhD candidates, and researchers.
  
## Pain points

  The mathematical sections of academic papers often suffer from unclear assumptions or overly concise derivations, making it difficult for readers to follow the reasoning. This hinders comprehension of key technical details, weakens understanding of the overall argument, and even obstructs the development of intuition in the field.

## Importance / urgency

  Reading academic papers is a central part of research and shapes how researchers choose and develop their own directions. Sometimes, an undergraduate, graduate student, or researcher is limited by their mathematical background and cannot fully understand papers in a certain field, forcing them to switch to another area. Yet many of these individuals may actually have strong potential—such as good intuition—and with enough mathematical support, they could make meaningful contributions. Their difficulty often comes not from a lack of effort, but from limitations in their educational background—for example, the quality of instruction at their undergraduate institutions. In math-intensive fields, helping researchers overcome this barrier could remove a major obstacle to understanding the literature and unlock significant research potential.

---

# Section 2: What You’ll Build ≤ 200 words
## Core offering

  A K2-Think–powered assistant for reading math-intensive papers, helping researchers understand key derivations and logical dependencies.

## User flow

 	1. Users can upload a PDF paper and read it within the GUI. They can select specific content and query K2-Think for explanations. 
	2. The GUI can iteratively ask K2-Think to generate a mind-map of the paper’s reasoning structure, which users can then edit manually.
	3. The GUI supports screenshot-based OCR for mathematical formulas. The recognized content is converted to LaTeX, reviewed and typed by the user, and stored in a math content list.
	4. Users may also upload their own math content, such as handwritten derivations recognized via OCR, or directly input LaTeX code.
	5. From the math content list, users can select one or more items and ask K2-Think specific questions—for example, “What role does Assumption 1 play in deriving Equation 1?” or “Check whether Derivation 1 contains a logical error.”

  1. 用户可以上传某论文的pdf文件，在GUI里阅读。用户可以选择内容[^3.5]，询问K2-Think。
  2. GUI可以迭代地询问 K2-Think，从而生成论文的思维导图[^7]。用户可以根据自己的理解，对该思维导图进行编辑。
  3. GUI支持截图OCR识别数学公式。数学公式识别为 LaTex 代码[^4]，经过用户修订并标记类型[^3]后，进入**数学内容**存储列表。
  4. 用户还可以上传自己的**数学内容**。例如，GUI支持对手写推导过程的OCR识别[^6]，用户可以修订识别出的 LaTex 代码，也可以直接上传 LaTex 代码。
  5. 用户可以从**数学内容**存储列表中勾选一个或多个**数学内容**，让 K2-Think 回答自己的问题。例如，“**假设1**在**公式1**的推导中起到了什么作用？”，“检查**推导1**是否存在缺陷。”

  [^3]: 类型包括但不限于假设、方程、公式、定理、引理、推导、证明
  [^3.5]: PyMuPDF + tkinter 即可实现（据ChatGPT）
  [^4]: MathPix API（据ChatGPT）
  [^6]: MathPix API（据ChatGPT）
  [^7]: graphML + tkinter 可以实现（据ChatGPT）
  
## Platform / tech stack
  - 总体GUI -> PyMuPDF，tkinter
  - 截图询问 -> OpenCV，Pillow（PIL），pytesseract
  - 思维导图 -> GraphML，tkinter
  - OCR识别pdf数学公式 -> MathPix API（每月免费100次，付费4.99$每月）
  - OCR识别手写数学公式 -> MathPix API

    
## Anything else you want to highlight

  - 确保推理结果的可靠性
   由于 AI 在推导过程中有时可能生成误导性或逻辑不一致的结论，系统将要求 **K2-Think 在进行任何推理前，必须先明确列出所有前提假设**。
   这样用户可以在推理前核查假设条件，从而有效避免错误结论的产生。

---

# Section 3: Why K2 Think ≤ 60 words
## Which specific capability of K2 Think are you leveraging?

  1. 论文阅读是一个连贯的智力过程，如果AI大模型的反应时间太长，将会破坏这种连贯性，造成理解困难。K2-Think的token速度能避免这类问题。
  2. 数学密集型的论文，其理解难点主要在于数学推理。K2-Think的高级数学推理能力，与该任务完美匹配。
     
---

# Section 4: Demo ≤ 50 words
## MVP[^mvp] you can realistically deliver in 48 hours

  [^mvp]: Minimum Viable Product

  1. A lightweight Python GUI
  2. Users can upload and view a PDF paper
  3. Users can screenshot a **mathematical content**, and get OCRed LaTex code (editable) which can then be added to the **math content list**.
  4. Users can choose from the **math content list** and get K2-think's response to their questions.

  一个轻量级的 Python 图形界面，用户可以上传并阅读 PDF，截取数学内容截图识别为可编辑的 LaTeX，保存到数学内容列表中，或直接上传自己的推导过程的LaTex代码，并选择其中的内容向 K2-Think 提问以获取推理解释。
  
  A lightweight Python GUI where users upload and read PDFs, capture math content as screenshots for editable LaTeX, save it to a math content list or upload their own LaTeX derivations, and query K2-Think for reasoning explanations based on selected items.

---

# Section 5: Support Needed (Optional · ≤ 30 words)
-	Credits, mentorship, dataset, etc.

  MathPix API
