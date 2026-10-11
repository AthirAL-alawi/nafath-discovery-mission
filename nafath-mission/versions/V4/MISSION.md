# Mission NAFATH-V4: Securing the Software Supply Chain

**Your version code:** `NAFATH-V4`
Complete this version only if it is the version code in your invitation email.

## The scenario

A national service provider must make sure that the software, AI models and internet routes it depends on cannot be secretly compromised.

Your job is to research how six IT fields apply to this scenario and write a short,
professional brief that a project manager could read in five minutes.

## The six research questions

Answer each question in its own section of your brief.

| Field | Research question |
|---|---|
| Software | According to the Twelve-Factor App methodology, where should configuration and secrets be stored, and why should they not be in the code? |
| AI | What are the main categories of adversarial attacks on machine learning systems (for example evasion and poisoning), and how do they differ? |
| Mobile | What is the OWASP Mobile Application Security Verification Standard (MASVS), and how is it used to verify the security of a mobile app? |
| Networking | How can BGP route hijacking redirect internet traffic, and how does RPKI help prevent it? What does RPKI not protect against? |
| Cybersecurity | What was the Log4Shell vulnerability (CVE-2021-44228), why was it rated so severe, and how was it fixed? |
| Data | What is a Software Bill of Materials (SBOM), and what minimum data fields should it contain? |

---

## Part 1: Write your brief

Your brief is one file named `brief.md`. Start from
[brief-template.md](brief-template.md). Do not change the headings.

### Writing rules

| Section | Length | What to write |
|---|---|---|
| Version line | 1 line | `Version: NAFATH-V4` (exactly) |
| Track line | 1 line | Your track: Software, AI, Mobile, Networking, Cybersecurity or Data |
| Overview | 100 to 150 words | How the six fields connect in this scenario |
| Each of the six fields | 50 to 80 words, plus one Resource line | Your answer to that field's research question |
| Misconception in My Track | 60 to 120 words | One common wrong belief about **your own track's** question, the correct version, and the section or heading in your resource that proves it |
| Open Question | Up to 50 words | One thing you would verify or learn next |

### Resource rules

- Under each of the six fields, add **exactly one** line in this format, after your answer:

  `Resource: <title of the page or document> - <full URL>`

- The resource must be a page you opened and read yourself.
- At least **four** of your six resources must be **official or primary**:
  standards and specifications (for example IETF RFCs, NIST, 3GPP), laws and
  regulators, official documentation, or published research papers.
- Do not use search result pages, AI chatbot links or social media posts.

### Example of one completed field (format only, different topic)

```
## Networking

QUIC is a transport protocol that runs over UDP and has TLS 1.3 encryption
built in. It sets up connections faster than TCP with TLS, and a lost packet
only delays its own stream instead of all streams. HTTP/3 runs on QUIC.
Connection IDs let a session survive when a phone switches from Wi-Fi to
mobile data, but some corporate firewalls block UDP, so a fallback is needed.

Resource: RFC 9000 - QUIC: A UDP-Based Multiplexed and Secure Transport - https://www.rfc-editor.org/rfc/rfc9000
```

---

## Part 2: Deliver it with an exact commit sequence

Create a **public** repository named `nafath-brief` with a README
(see [GITHUB_HELP.md](../../GITHUB_HELP.md), Parts 1 and 2).
Then complete these seven steps **in order**, all on the `main` branch.

**Each step is one commit.** Each commit changes **only** the sections named in that step.
Commit messages must match **exactly**, in lowercase.

| Step | What to do | Exact commit message |
|---|---|---|
| 1 | Create `brief.md` from the template. Fill in only the `Version:` and `Track:` lines. Leave all sections empty. | `skeleton: NAFATH-V4` |
| 2 | Write the **Overview**. | `overview: connect the six subtopics` |
| 3 | Write **Software**, **AI** and **Mobile**, each with its Resource line. | `research: software, ai, mobile` |
| 4 | Write **Networking**, **Cybersecurity** and **Data**, each with its Resource line. | `research: networking, cybersecurity, data` |
| 5 | Write **Misconception in My Track** and **Open Question**. | `analysis: misconception and open question` |
| 6 | Edit **only the Overview**, so that its **last sentence** names the topic of your own track's question. Keep it within 150 words. | `revise: overview` |
| 7 | Create a new file `CHANGELOG.md` listing the commit IDs of steps 1 to 6 (see below). | `changelog: record history` |

### CHANGELOG.md format

List the **7-character commit ID** and the commit message of steps 1 to 6,
**oldest first**, one per line, exactly like this:

```
- 1a2b3c4 skeleton: NAFATH-V4
- 5d6e7f8 overview: connect the six subtopics
- 9a8b7c6 research: software, ai, mobile
- 5e4d3c2 research: networking, cybersecurity, data
- 1f2e3d4 analysis: misconception and open question
- 6c5b4a3 revise: overview
```

(These IDs are examples. Use your real IDs. GITHUB_HELP.md explains where to find them.)

### Rules

1. Work only on the `main` branch. Do not create branches.
2. Never edit `README.md`.
3. Do not add any files other than `brief.md` and `CHANGELOG.md`.
4. Do not delete and re-create `brief.md`. Always edit it.
5. If you make a mistake, fix it with an extra commit whose message starts with
   `fix:`. Do not rewrite history.
6. Do not change your repository after you submit the form, except to fix a problem
   before the deadline (and then submit the form again).

---

## Part 3: Submit the form

When all seven steps are done, open the submission form from your invitation email.
You will need:

- Your repository URL, for example `https://github.com/your-username/nafath-brief`
- The 7-character ID of your **last** commit (the `changelog` commit)
- The exact sentence from your resource that supports your Misconception section

Deadline: **[Tuesday, DD Month YYYY] at 11:59 PM, Oman time (GMT+4)**.

## Final checklist

- [ ] `brief.md` has the Version line `NAFATH-V4` and your Track line
- [ ] All 9 section headings are unchanged
- [ ] Every section is within its word limits, in English
- [ ] Exactly one Resource line under each of the six fields
- [ ] At least four resources are official or primary
- [ ] Seven commits, in order, with exact messages
- [ ] `CHANGELOG.md` lists steps 1 to 6, oldest first, with correct IDs
- [ ] `README.md` unchanged; no other files added
- [ ] Repository is public (checked in a private browser window)
- [ ] Form submitted
