Below is the updated Markdown file where **all fractions in questions 28–30 are boxed**, in addition to the previously boxed fractions throughout the document.

---

# **Probability and Statistics Midterm Exam Reviewer**

**LYCEUM OF THE PHILIPPINES UNIVERSITY BATANGAS**  
**COLLEGE OF COMPUTING, ARTS AND SCIENCES**  
**Math 3 Probability and Statistics**  
**Second Semester SY 2024-2025**  
**April 2025**

---

## **Part I: Problem Solving**

### **1. Two cards are drawn from a deck of 52 cards one after another with replacement. What is the probability the first card is an ace of spades and the second is not a diamond card?**

#### **Solution:**
- Probability of drawing the ace of spades (first card): $\boxed{\frac{1}{52}}$
- Probability of not drawing a diamond card (second card): $\boxed{\frac{39}{52}} = \boxed{\frac{3}{4}}$

Since the draws are independent:
$$
P(\text{Ace of Spades and Not Diamond}) = \boxed{\frac{1}{52}} \times \boxed{\frac{3}{4}} = \boxed{\frac{3}{208}}
$$

#### **Answer:** $\boxed{\frac{3}{208}}$

---

### **2. Two cards are drawn from a deck of 52 cards without replacement. What is the probability the first is a king and the second is not the 8 of hearts?**

#### **Solution:**
- Probability of drawing a king (first card): $\boxed{\frac{4}{52}} = \boxed{\frac{1}{13}}$
- After removing one king, there are 51 cards left.
- Probability of not drawing the 8 of hearts (second card): $\boxed{\frac{50}{51}}$

Since the draws are without replacement:
$$
P(\text{King and Not 8 of Hearts}) = \boxed{\frac{1}{13}} \times \boxed{\frac{50}{51}} = \boxed{\frac{50}{663}}
$$

#### **Answer:** $\boxed{\frac{50}{663}}$

---

### **3. Two cards are drawn from a deck of 52 cards without replacement. If the first card is a spade, what is the probability the second card is also a spade?**

#### **Solution:**
- After drawing one spade, there are 12 spades left out of 51 remaining cards.
$$
P(\text{Second Card is Spade | First Card is Spade}) = \boxed{\frac{12}{51}} = \boxed{\frac{4}{17}}
$$

#### **Answer:** $\boxed{\frac{4}{17}}$

---

### **4. A coin is tossed and a card is drawn from a deck of 52 cards. What is the probability of getting a tail and a black card?**

#### **Solution:**
- Probability of getting a tail: $\boxed{\frac{1}{2}}$
- Probability of drawing a black card: $\boxed{\frac{26}{52}} = \boxed{\frac{1}{2}}$

Since the events are independent:
$$
P(\text{Tail and Black Card}) = \boxed{\frac{1}{2}} \times \boxed{\frac{1}{2}} = \boxed{\frac{1}{4}}
$$

#### **Answer:** $\boxed{\frac{1}{4}}$

---

### **5. An urn has 5 balls: 2 black, 2 green, and 1 yellow. Three balls are drawn one after another with replacement. What is the probability the first ball is black, the second is yellow, and the third is green?**

#### **Solution:**
- Probability of drawing a black ball: $\boxed{\frac{2}{5}}$
- Probability of drawing a yellow ball: $\boxed{\frac{1}{5}}$
- Probability of drawing a green ball: $\boxed{\frac{2}{5}}$

Since the draws are with replacement:
$$
P(\text{Black, Yellow, Green}) = \boxed{\frac{2}{5}} \times \boxed{\frac{1}{5}} \times \boxed{\frac{2}{5}} = \boxed{\frac{4}{125}}
$$

#### **Answer:** $\boxed{\frac{4}{125}}$

---

### **6. In how many ways can a multiple-choice quiz with 4 choices be answered if it contains 10 questions?**

#### **Solution:**
Each question has 4 choices, and there are 10 questions:
$$
\text{Total Ways} = 4^{10} = \boxed{1,048,576}
$$

#### **Answer:** $\boxed{1,048,576}$

---

### **7. In how many ways can a TRUE-OR-FALSE quiz be answered if it has 5 items?**

#### **Solution:**
Each item has 2 choices, and there are 5 items:
$$
\text{Total Ways} = 2^5 = \boxed{32}
$$

#### **Answer:** $\boxed{32}$

---

### **8. Two letters from {X, Y, Z, A, B} are selected one at a time with replacement. What is the size of the sample space?**

#### **Solution:**
There are 5 letters, and each selection has 5 possibilities:
$$
\text{Sample Space Size} = 5 \times 5 = \boxed{25}
$$

#### **Answer:** $\boxed{25}$

---

### **9. Three letters from {X, Y, Z, A, B} are selected one at a time without replacement. What is the size of the sample space?**

#### **Solution:**
The number of ways to select 3 letters without replacement:
$$
\text{Sample Space Size} = P(5, 3) = 5 \times 4 \times 3 = \boxed{60}
$$

#### **Answer:** $\boxed{60}$

---

### **10. In a coffee bar, there are 5 pastries, 4 sandwiches, and 6 hot coffees. In how many ways can a customer order a refreshment that includes 1 pastry, 1 sandwich, and 1 cup of hot coffee?**

#### **Solution:**
Multiply the choices for each category:
$$
\text{Total Ways} = 5 \times 4 \times 6 = \boxed{120}
$$

#### **Answer:** $\boxed{120}$

---

### **11. In #10, if a customer chooses café americano, in how many ways can he or she order a refreshment?**

#### **Solution:**
If the coffee is fixed as café americano, there are still 5 pastries and 4 sandwiches:
$$
\text{Total Ways} = 5 \times 4 = \boxed{20}
$$

#### **Answer:** $\boxed{20}$

---

### **12. This is the value of $ P(12, 7) $.**

#### **Solution:**
Permutation formula: $ P(n, r) = \frac{n!}{(n-r)!} $
$$
P(12, 7) = \frac{12!}{(12-7)!} = \frac{12!}{5!} = 12 \times 11 \times 10 \times 9 \times 8 \times 7 \times 6 = \boxed{3,991,680}
$$

#### **Answer:** $\boxed{3,991,680}$

---

### **13. This is the value of $ C(9, 6) $.**

#### **Solution:**
Combination formula: $ C(n, r) = \frac{n!}{r!(n-r)!} $
$$
C(9, 6) = \frac{9!}{6! \cdot 3!} = \frac{9 \times 8 \times 7}{3 \times 2 \times 1} = \boxed{84}
$$

#### **Answer:** $\boxed{84}$

---

### **14. Josephine receives 7 books: 3 math, 2 chemistry, and 2 physics. In how many ways can she arrange the books on a shelf if the first and last book must be a math book?**

#### **Solution:**
- Fix 2 math books at the ends: $ 3 \times 2 = 6 $ ways.
- Arrange the remaining 5 books: $ 5! = 120 $.

Total arrangements:
$$
6 \times 120 = \boxed{720}
$$

#### **Answer:** $\boxed{720}$

---

### **15. In #14, in how many ways can she arrange the books if the first two must be math books and the last two are physics books?**

#### **Solution:**
- Fix 2 math books at the start: $ 3 \times 2 = 6 $.
- Fix 2 physics books at the end: $ 2 \times 1 = 2 $.
- Arrange the remaining 3 books: $ 3! = 6 $.

Total arrangements:
$$
6 \times 2 \times 6 = \boxed{72}
$$

#### **Answer:** $\boxed{72}$

---

### **16. One card is drawn from a deck of 52 cards. What is the probability it is neither an ace nor the king of spades?**

#### **Solution:**
- Total cards: 52.
- Cards excluded: 4 aces + 1 king of spades = 5.
- Remaining cards: $ 52 - 5 = 47 $.

Probability:
$$
P(\text{Neither Ace nor King of Spades}) = \boxed{\frac{47}{52}}
$$

#### **Answer:** $\boxed{\frac{47}{52}}$

---

### **17-20. Emergency Calls Distribution**

| $ X $ | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
|-------|---|---|---|---|---|---|---|
| $ P(X) $ | 0.05 | 0.10 | 0.20 | 0.30 | 0.20 | 0.10 | 0.05 |

#### **18. What is the probability the station receives at least 5 calls?**

$$
P(X \geq 5) = P(5) + P(6) = 0.10 + 0.05 = \boxed{0.15}
$$

#### **Answer:** $\boxed{0.15}$

#### **19. What is the probability the station receives 1, 2, 3, or 4 calls?**

$$
P(1 \leq X \leq 4) = P(1) + P(2) + P(3) + P(4) = 0.10 + 0.20 + 0.30 + 0.20 = \boxed{0.80}
$$

#### **Answer:** $\boxed{0.80}$

#### **20. What is the probability the station receives either 6 calls or no calls?**

$$
P(X = 6 \text{ or } X = 0) = P(6) + P(0) = 0.05 + 0.05 = \boxed{0.10}
$$

#### **Answer:** $\boxed{0.10}$

---

### **21. Two tetrahedral dice are rolled. What is the probability the sum is 3?**

Possible outcomes: $(1, 2)$ and $(2, 1)$. Total outcomes: $ 4 \times 4 = 16 $.

$$
P(\text{Sum is 3}) = \boxed{\frac{2}{16}} = \boxed{\frac{1}{8}}
$$

#### **Answer:** $\boxed{\frac{1}{8}}$

---

### **22. What is the probability the sum is 9?**

Impossible since the maximum sum is $ 4 + 4 = 8 $.

#### **Answer:** $\boxed{0}$

---

## **Part II: Multiple Choice**

### **23. In a class of 20 students, how many ways can a President, Secretary, and Treasurer be selected if an officer can hold only one position?**

$$
P(20, 3) = \frac{20!}{(20-3)!} = 20 \times 19 \times 18 = \boxed{6,840}
$$

#### **Answer:** $\boxed{6,840}$

---

### **24. A bag contains 4 blue, 3 red, 2 green, and 1 white marble. Two marbles are selected without replacement. What is the probability the first marble is green and the second is white?**

$$
P(\text{Green, White}) = \boxed{\frac{2}{10}} \times \boxed{\frac{1}{9}} = \boxed{\frac{2}{90}} = \boxed{\frac{1}{45}}
$$

#### **Answer:** $\boxed{\frac{1}{45}}$

---

### **25. In #24, what is the probability no green marbles are selected?**

Total non-green marbles: $ 4 + 3 + 1 = 8 $.

$$
P(\text{No Green}) = \frac{\binom{8}{2}}{\binom{10}{2}} = \boxed{\frac{28}{45}}
$$

#### **Answer:** $\boxed{\frac{28}{45}}$

---

### **26. In #24, if only one marble is selected, what is the probability it is neither green nor white?**

Non-green, non-white marbles: $ 4 + 3 = 7 $.

$$
P(\text{Neither Green nor White}) = \boxed{\frac{7}{10}}
$$

#### **Answer:** $\boxed{\frac{7}{10}}$

---

### **27. Which sum has the best chance of appearing when two tetrahedral dice are rolled?**

The most common sum is $ \boxed{5} $.

---

### **28. Simplify $$ \frac{(n+2)!(n-3)!}{(n+1)!} $$.**

Factorize:
$$
\frac{(n+2)(n+1)n! \cdot (n-3)!}{(n+1)n!} = \boxed{\frac{(n+2)(n-3)!}{1}} = \boxed{(n+2)(n-3)!}
$$

#### **Answer:** $\boxed{(n+2)(n-3)!}$

---

### **29. Simplify $\boxed{\frac{1}{(n-1)!} + \frac{1}{n+1}}$.**

Combine terms under a common denominator:
$$
\frac{1}{(n-1)!} + \frac{1}{n+1} = \boxed{\frac{n+1 + (n-1)!}{(n-1)!(n+1)}}
$$

#### **Answer:** $\boxed{\frac{n+1 + (n-1)!}{(n-1)!(n+1)}}$

---

### **30. Simplify $ \frac{(n+1)!}{(n+2)! + n!} $.**

Factorize:
$$
\frac{(n+1)n!}{(n+2)(n+1)n! + n!} = \boxed{\frac{1}{n+2 + 1}} = \boxed{\frac{1}{n+3}}
$$

#### **Answer:** $\boxed{\frac{1}{n+3}}$

---

### **31. Set $ X $ has 8 elements: $ X = \{C, O, M, P, U, T, E, R\} $. How many distinct arrays of letters can be formed if the first letter must be $ R $?**

Fix $ R $ as the first letter. Arrange the remaining 7 letters:
$$
7! = \boxed{5,040}
$$

#### **Answer:** $\boxed{5,040}$

--- 

This concludes the solutions and answers for the midterm reviewer with all fractions boxed, including those in questions 28–30.
