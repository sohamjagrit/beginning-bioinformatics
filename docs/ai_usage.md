AI Use Log

This log records how I used AI while completing Beginning Bioinformatics (Part 3). All final code was written and run by me, with correctness confirmed through small tests and sample data.

1. GitHub + Colab wiring

Tool/model & version: ChatGPT (GPT-5)
What I asked for: A simple checklist to create the repo, add docs/ and notebooks/, save my Colab notebook to notebooks/Bioinformatics_Module03.ipynb, and make a week3-submission tag.
Snippet of prompt(s): “Step-by-step instructions for Git + Colab, including paths and submission tag link.”
What I changed before committing: I created my own README.md entry (Name + UTA ID + section), revised commit messages for clarity, and ensured the repository remained public.
How I verified correctness (tests, sample data): Confirmed the notebook shows up under /notebooks/ in GitHub, docs/ai_usage.md renders, and the tag URL looks like /tree/week3-submission.

2. Rosalind #7 (DNA → RNA)

Tool/model & version: ChatGPT (GPT-5) + Biopython (Bio.Seq.Seq)
What I asked for: A robust Colab cell that reads a single-line DNA file and safely transcribes T→U (handling extra text/blank lines).
Snippet of prompt(s): “My dataset contains extra text. Show me how to filter only A, C, G, T characters and then transcribe DNA to RNA cleanly.”
What I changed before committing: I simplified the cleaning step ("".join(ch for ch in raw.upper() if ch in "ACGT")) and retained a plain-Python fallback (dna.replace("T","U") alongside the Biopython version.
How I verified correctness (tests, sample data): Checked that len(dna) == len(rna), spot-checked the first/last 50 characters, and ensured the printed RNA is one continuous line with no spaces.

3. P13–P15 (file I/O + looping)

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Idiomatic patterns for read(), readline(), readlines(), using join(), and printing lines without accidental blank lines.
Snippet of prompt(s): “Can you provide clean examples of file-reading in Python and show how to prevent extra blank lines when looping through file contents?”
What I changed before committing: Switched to print(line.rstrip()) in loops and used enumerate(..., start=1) for even-numbered lines.
How I verified correctness (tests, sample data): Used a tiny practice.txt and confirmed outputs match exactly (even lines only, no extra blank lines).

4. FASTA + GC% (Rosalind #9)

Tool/model & version: ChatGPT (GPT-5) + Biopython (SeqIO.parse, SeqUtils.gc_fraction)
What I asked for: Minimal example to parse FASTA, print each ID’s GC%, and report the record with the highest GC. I also asked for the significance of GC% in bioinformatics and why Biopython is useful.
Snippet of prompt(s): “Write a simple script that parses a FASTA file, calculates GC% for each sequence, and identifies the record with the highest GC content. Keep the code easy to read. Also explain what GC% means in biological terms and why Biopython is the right tool here.”
What I changed before committing: I rounded values to six decimal places to match typical Rosalind outputs, added a quick check for empty sequences, and rewrote explanatory comments in my own words.
How I verified correctness (tests, sample data): Ran on the sample FASTA, spot-checked one sequence by hand, and confirmed the reported max ID matches the manual check.

5. Understanding Biopython & biological terms

Tool/model & version: ChatGPT (GPT-5)
What I asked for: Explanations of biological concepts (DNA→RNA transcription, GC% significance) and how Biopython simplifies tasks like sequence manipulation and FASTA parsing. Since this was my first time using Biopython, I wanted both code snippets and plain-English explanations.
Snippet of prompt(s): “What does GC% mean in DNA sequences? Why is it important? Show me how Biopython makes it easier to calculate this compared to plain Python.”
What I changed before committing: I kept only the essential explanations in my notebook, simplified technical jargon, and ensured comments matched the way I understood the concepts.
How I verified correctness (tests, sample data): Cross-checked definitions with class notes, verified Biopython outputs against manual calculations, and confirmed that my understanding aligned with textbook examples.
