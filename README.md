

# ✅ Google Dorking Cheatsheet
_A beginner-friendly guide for ethical hackers, researchers, and learners._

---

## 🧠 What is Google Dorking?

Google Dorking (also known as Google hacking) uses advanced search operators to find publicly available but often overlooked data. These queries are powerful tools for **security research**, **reconnaissance**, and **data discovery**.

---

## ⚠️ Ethics Disclaimer
> This cheatsheet is for **educational and ethical** use only.  
> Never attempt to access, exploit, or harm systems or data you don’t have permission to use.

---

## 🔍 Basic Operators

| Operator       | Description                            | Example                          |
|----------------|----------------------------------------|----------------------------------|
| `site:`        | Search within a specific domain        | `site:example.com`               |
| `filetype:`    | Find specific file types               | `filetype:pdf`                   |
| `intitle:`     | Search page titles                     | `intitle:"index of"`             |
| `inurl:`       | Search in URLs                         | `inurl:admin`                    |
| `intext:`      | Search page body content               | `intext:"confidential"`          |
| `cache:`       | Show Google's cached version           | `cache:example.com`              |

---

## 🧪 Common Dorks for Security Research

| Goal                        | Dork Example                                                 |
|-----------------------------|--------------------------------------------------------------|
| Find exposed login pages    | `inurl:login` or `intitle:"Admin Login"`                    |
| List open directories       | `intitle:"index of /" + "parent directory"`                 |
| Find exposed SQL files      | `filetype:sql intext:"password"`                            |
| Locate config files         | `filetype:env OR filetype:xml intext:"password"`            |
| Discover sensitive PDFs     | `filetype:pdf intext:"confidential"`                        |
| Search WordPress logins     | `inurl:wp-admin`                                             |

---

## 🤖 AI + Cybersecurity Focused Dorks

| Purpose                            | Dork Example                                                                 |
|-----------------------------------|-------------------------------------------------------------------------------|
| Find ML papers (edu)              | `site:.edu "machine learning" filetype:pdf`                                  |
| Find datasets                     | `"dataset" "machine learning" filetype:csv`                                  |
| Open Jupyter Notebooks            | `intitle:"Jupyter Notebook" inurl:/notebooks/`                               |
| Public Hugging Face Spaces        | `site:huggingface.co/spaces`                                                 |
| TensorBoard Dashboards            | `intitle:"TensorBoard" inurl:/data/`                                         |

---

## 🌐 Tools That Help With Dorking

| Tool           | Purpose                             | Link                              |
|----------------|-------------------------------------|-----------------------------------|
| Shodan         | Device & IoT search engine          | [https://shodan.io](https://shodan.io) |
| Censys         | Find public servers, certs, ports   | [https://censys.io](https://censys.io) |
| Perplexity AI  | Semantic AI search                  | [https://perplexity.ai](https://perplexity.ai) |
| Phind          | Developer + security AI search      | [https://phind.com](https://phind.com) |

---

## ✅ Example Use Case

```bash
site:gov filetype:xls intext:"email"
```
> Finds Excel files on government websites that contain the word "email" – useful for awareness on data exposure.

---

## 📁 License

This repository is licensed under the [MIT License](LICENSE).  
Use it to **learn, document, and educate**, not for unethical activity.
