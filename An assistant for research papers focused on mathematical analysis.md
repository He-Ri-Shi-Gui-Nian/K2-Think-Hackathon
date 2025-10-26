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
  3. The GUI supports screenshot-based OCR for mathematical formulas. The recognized formulas are converted into LaTeX code, which users can review, modify, and label by type (including but not limited to assumptions, equations, formulas, theorems, lemmas, derivations, and proofs). The processed items are then stored in the Math Content List.
  4. Users may also upload their own math content, such as handwritten derivations recognized via OCR, or directly input LaTeX code.
  5. From the math content list, users can select one or more items and ask K2-Think specific questions—for example, “What role does Assumption 1 play in deriving Equation 1?” or “Check whether Derivation 1 contains a logical error.”
  
## Platform / tech stack
- Overall GUI: PyMuPDF, tkinter
- Screenshot OCR: OpenCV, Pillow (PIL), pytesseract
- Mind-map visualization: GraphML, tkinter
- OCR for printed/handwritten math formulas: MathPix Convert API

    
## Additional Notes

To ensure reliability of reasoning, K2-Think will be required to explicitly list all assumptions before performing any derivation.
This allows users to verify premises in advance and prevents logically inconsistent or misleading conclusions.

---

# Section 3: Why K2 Think ≤ 60 words
## Which specific capability of K2 Think are you leveraging?

- Academic reading is a continuous cognitive process; long model latency disrupts comprehension. K2-Think’s fast token streaming maintains this flow.
- The main difficulty in math-intensive papers lies in logical reasoning. K2-Think’s advanced mathematical inference capability is perfectly suited for this task.
     
---

# Section 4: Demo ≤ 50 words
## MVP you can realistically deliver in 48 hours
  
  A lightweight Python GUI where users upload and read PDFs, capture math content as screenshots for editable LaTeX, save it to a math content list or upload their own LaTeX derivations, and query K2-Think for reasoning explanations based on selected items.

---

# Section 5: Support Needed (Optional · ≤ 30 words)

- Access to the MathPix Convert API
- Guidance on the effective use of the K2-Think API.
