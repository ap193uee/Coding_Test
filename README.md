# Curl Analytics Coding Test
Sample files for coding test of Curl Analytics

### Instructions
* Submit the answers in Python format only.
  * Download the sample files for the questions from this repository
  * Add your code in the corresponding files
  * Email the code files to atinder@curlanalytics.com with subject **IITB Recruitment Test**
  * The subject line should be exact otherwise your email will be discarded.
  * Also share your github profile link if present in the email. 
* Clean code with proper comments and coding style will be preferred.
* Scoring will be done based on number of test cases passed and the coding style.
---

### Question 1
Write a function to extract the date patterns from a given text string. Don’t use any libraries (e.g date-extractor, spacy) to extract date. You can use datetime or similar libraries only to validate (not extract) the extracted date. Here are some example date formats for your reference:

1. OCT.04,2018
2. 19 September, 2018
3. 2018/9/20
4. 05.10.2016
5. 9th day of month February of year 2017
6. 18-OCT-2018
7. 23-Oct-18
8. Oct 17, 2018 
9. 2018/10/23
10. 19th of September, 2018.

> Note: Ensure only **valid** dates are extracted. For ex : 32/12/2019 is invalid  
> The function should handle variation in **space**, combination of (-.,/) and should be **case** insensitive  
> **Hint: Use regex**

**Function format**: extract_date(query_string) --> extracted_date_string  
**Function name**: extract_date  
**Arguments**: query_string (contains max 1 date)  
**Returns**: date_extracted (type string)  

#### Sample Inputs
* Payment is due on Oct 17, 2018. Please pay 95 percent on or before this date.
* Lorem ipsum 24/7 Lorem ipsum.

#### Sample Output
* Oct 17, 2018
* None
---

### Question 2
You have a string of lowercase English alphabets. You can perform only two types of operations on the string:

1. **Append** a lowercase English alphabetic letter to the end of the string.
2. **Delete** the last character in the string. Performing this operation on an empty string results in an empty string.

Given an integer, k, and two strings, s and t, determine whether or not you can convert s to t by performing exactly k of the above operations on s.

**Function format**: is_convertible(k, s, t) --> boolean  
**Function Name**: is_convertible  
**Arguments**: k, s, t  
**Returns**: boolean (True or False)  

#### Constraints
0 ≤ k ≤ 100  
0 ≤ len(s) ≤ 100  
0 ≤ len(t) ≤ 100  

#### Sample Input
k=5  
s=whoareyou  
t=whoarewe  

#### Sample Output
True

#### Explanation
As we can delete (y,o,u) and add (w,e) in exactly 5 moves  
if k=6 then output is False  
If k=7 then out is True as we could delete (e,y,o,u) and add (e,w,e) in exactly 7 moves )
