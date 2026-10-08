# secrets-in-source-2-writeup
A professional writeup for the HackerDNA lab “Secrets in Source 2: Bypass Security Through Obscurity.” Includes methodology, tools used, insights, and key learnings. No flag content disclosed.

# Secrets in Source 2 – Writeup

🔗 Lab Reference: [Secrets in Source 2: Bypass Security Through Obscurity](https://hackerdna.com/labs/secrets-in-source-2)

## 🎯 Objective
Learn how attackers bypass superficial restrictions (like blocked right-click or disabled source view) and uncover hidden files through persistence and alternative methods.

## 🛠 Tools & Techniques Used
- Web Browser (with Developer Tools)
- Command-line utilities (`curl`, `wget`)
- Browser settings (disable JavaScript)
- URL manipulation and directory guessing
- Optional: Burp Suite or HTTPie for request inspection

## 🔎 Methodology
1. **Explored the Lab Page**  
   - Opened the challenge URL and noted restrictions (blocked right-click, disabled source view).  

2. **Tried Alternative Access Methods**  
   - Used `curl` to fetch the raw HTML directly.  
   - Disabled JavaScript in browser settings to bypass restrictions.  

3. **Searched for Clues**  
   - Examined HTML comments and hidden references.  
   - Looked for unusual directory names or file paths.  

4. **Followed Breadcrumbs**  
   - Constructed possible URLs (`/flag.txt`, `/hidden/flag.txt`, `/challenge/flag.txt`).  
   - Navigated directly to these paths until the correct file was found.  

5. **Retrieved and Submitted the Flag**  
   - Copied the UUID-style flag string (not disclosed here).  
   - Submitted it in the lab’s flag box to complete the challenge.  

---

## 📚 Key Learnings
- **Security Through Obscurity Fails**: Blocking right-click or hiding files in odd directories does not secure sensitive data.  
- **Persistence Pays Off**: Attackers use multiple tools and methods to bypass restrictions.  
- **Systematic Approach**: Always check source code, robots.txt, hidden paths, and try direct URL access.  

---

## ⚡ Challenges Faced
- Encountered misleading error messages (`NoSuchKey`) when accessing incorrect paths.  
- Learned to try small variations in directory names to uncover the correct location.  

---

## 🚀 Insights for Future Labs
- Build a checklist for obscurity challenges:  
  - Try direct URL paths (`/flag.txt`, `/secret/flag.txt`).  
  - Check `robots.txt` and `sitemap.xml`.  
  - Use CLI tools to bypass browser restrictions.  
- Document each step for repeatable workflows.  
- Reinforce the principle: **real security requires proper access controls, not hiding files.**

