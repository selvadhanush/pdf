# pdf# Replacing en-dash (–) with a regular hyphen (-) to ensure compatibility with latin-1 encoding

# Clean and reformat the data to avoid all special characters
clean_schedule = [
    ("Day 1", "Arrays and Quant Basics", "2 LeetCode problems on Arrays (Easy to Medium)", 
     "Practice 10-15 questions on Percentages and Ratios", 
     "Prepare your 'Tell me about yourself' and resume pitch"),
    
    ("Day 2", "Strings and Time Speed Distance", "2 LeetCode problems on Strings",
     "10 questions on Time, Speed and Distance", 
     "Review your past projects (be ready to explain your code and stack)"),
    
    ("Day 3", "Recursion and Logical Reasoning", "1 Recursion and 1 Backtracking problem",
     "Puzzles and Seating Arrangement (10 questions)", 
     "Revise OOPs concepts with real-life examples"),
    
    ("Day 4", "Sorting and Profit Loss", "Implement and understand 2 sorting algorithms",
     "10 questions on Profit and Loss", 
     "Prepare answers for 'Why Morgan Stanley?' and 'Your strengths'"),
    
    ("Day 5", "Linked List and Probability", "2 Linked List problems",
     "10 Probability and Permutation questions", 
     "Mock test on DBMS (Joins, Normalization, Transactions)"),
    
    ("Day 6", "Trees and OS Concepts", "2 Tree problems (BST or Traversal)",
     "Practice Mixed Aptitude set (20 Questions)", 
     "OS Basics: Deadlock, Scheduling, Paging"),
    
    ("Day 7", "Review and Mock Day", "Revise all DSA topics attempted",
     "Take a full-length Aptitude test (from IndiaBix or GFG)", 
     "Mock HR and Technical interview session"),
]

# Reinitialize PDF generation with cleaned content
pdf = CleanPDF()
pdf.set_auto_page_break(auto=True, margin=15)

for day_info in clean_schedule:
    pdf.add_day(*day_info)

output_path = "/mnt/data/Morgan_Stanley_Preparation_Tracker.pdf"
pdf.output(output_path)
output_path
