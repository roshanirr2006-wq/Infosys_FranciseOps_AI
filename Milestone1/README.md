# Milestone 1
### Project Overview & Code Breakdown

The application is an immersive, multi-tiered **Franchise Portal** built with **Streamlit** and backed by an asynchronous-ready **SQLite database** architecture. It is styled with a custom fluid dark-synth aesthetic using a dedicated color palette (`#00f0ff` cyan, `#ff007f` magenta) injected directly through CSS overrides.

---

### 📂 Structural Breakdown & Application Flow

```
  [ Login Page ]  ──────► ( Validates Input / Role Checks )
         │                                │
         ├──► [ Sign Up Page ]            ├──► [ Admin Dashboard ] (admin@llm.com)
         │                                │       └── Registered Users Directory (Dataframe)
         └──► [ Forgot Password ]         │
                 │                        └──► [ Standard Dashboard ] (Franchise Members)
                 ├──► Via Security Q&A            ├── Home View (Core KPI Cards)
                 └──► Via Gmail OTP               └── Analytics View (Plotly Gauge Charts)

```

---

### 💻 Deep-Dive Module Breakdown

#### 1. Configuration & Theming Engine

* **Visual Styling:** Overrides default Streamlit constraints via dynamic markdown injections, substituting premium typefaces (`Space Grotesk` and `Plus Jakarta Sans`) and creating bioluminescent info cards with custom glassmorphic hover shadows.
* **Environment Mapping:** Automatically pairs local environments with cloud configurations by tracking runtime keys via Google Colab's secrets engine (`NGROK_AUTHTOKEN`, `EMAIL_ADDRESS`, `EMAIL_PASSWORD`, and `JWT_SECRET`).

#### 2. Cryptographic Security & Database Infrastructure

* **Storage Layer:** Uses an internal SQLite schema (`infosys_portal.db`) with two critical tracking nodes: `users` and `login_attempts`.
* **Password Hashing:** Implements one-way salting and verification loops via `bcrypt` to completely isolate cleartext strings from memory layers.
* **Session Management:** Uses cryptographically signed JSON Web Tokens (`PyJWT`) with automated 2-hour sliding expirations (`HS256` algorithm) to safely handle cross-page transitions.

#### 3. Strict Input Layout Validations

* **Email Ruleset:** Evaluates semantic structure profiles using strict regular expression captures (`^[a-zA-Z0-9._%+-]{2,}@[a-zA-Z0-9.-]{2,}\.[a-zA-Z]{2,}$`).
* **Password Blueprint:** Enforces structural integrity policies, requiring a minimum of 8 characters containing at least 1 uppercase letter, 1 lowercase letter, 1 numeric value, and 1 unique punctuation symbol.

#### 4. Dual Password Recovery & Verification Pipelines

* **Security Questions Setup:** Validates user profiles by checking cryptographically hashed responses to pre-registered identity queries.
* **Automated Gmail OTP Engine:** Generates highly randomized 6-digit session codes using Python's `secrets.randbelow` library. These temporary tokens are protected by a standalone JWT signature wrapper that automatically expires after 5 minutes. The dispatch engine operates on a secure standard TLS transport loop (`smtp.gmail.com:587`).

#### 5. Role-Based App Dashboards

* **Admin Management (`admin@llm.com`):** Grants master privileges to oversee system tables. It displays a comprehensive operations layout that outputs a dynamic `pandas` table tracking user database IDs, custom aliases, emails, and timestamp vectors.
* **Standard Franchise Member:** Grants access to standard business modules:
* **Core Dashboard Layer:** Displays visual tracking summaries, including metrics for *Documents Indexed*, *Searches Today*, and an overall *Efficiency Score*.
* **Analytics View:** Embeds real-time system performance data directly into responsive, interactive Plotly layout elements (*System Health Gauge Charts*).



---

### 📂 README-Ready Image Mapping Framework

You can organize your project submission file by structured feature components. The relative links below map directly to your local file pathing variables:

```markdown
### 🖼️ Core Interface References

### 🖼️ Core Interface References

#### 1. Identity Gateways & Verification Pipelines

* **Account Provisioning:** Dynamic structural setup validation.
  <a href="./Milestone1/screenshots/Create_Account.png" target="_blank">👉 Click here to view Create Account Snapshot</a>
  
  ![Create Account](./Milestone1/screenshots/Create_Account.png)

* **Central Login Gateway:** Core user validation checkpoint.
  <a href="./Milestone1/screenshots/Login_page.png" target="_blank">👉 Click here to view Login Page Snapshot</a>
  
  ![Login Page](./Milestone1/screenshots/Login_page.png)

* **Password Recovery Interface:** Route split configuration panel.
  <a href="./Milestone1/screenshots/Forgot_Password.png" target="_blank">👉 Click here to view Forgot Password Snapshot</a>
  
  ![Forgot Password](./Milestone1/screenshots/Forgot_Password.png)

* **Secure OTP Verification:** Multi-factor programmatic token synchronization.
  <a href="./Milestone1/screenshots/otp.png" target="_blank">👉 Click here to view OTP System Snapshot</a>
  
  ![OTP System](./Milestone1/screenshots/otp.png)

#### 2. Operations & Advanced Reporting Panels

* **Main KPI Dashboard View:** System indicator summary panel.
  <a href="./Milestone1/screenshots/Home_Dashboard.png" target="_blank">👉 Click here to view Home Dashboard Snapshot</a>
  
  ![Home Dashboard](./Milestone1/screenshots/Home_Dashboard.png)

* **Interactive Business Analytics:** Custom Plotly performance monitoring.
  <a href="./Milestone1/screenshots/Dashboard.png" target="_blank">👉 Click here to view Dashboard Layout Snapshot</a>
  
  ![Dashboard Layout](./Milestone1/screenshots/Dashboard.png)

```
