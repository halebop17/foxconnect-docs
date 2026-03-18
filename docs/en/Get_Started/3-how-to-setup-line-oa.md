---
icon: 
title: 3. How to setup LINE OA
---

# Setup LINE OA

<iframe width="560" height="315" src="https://www.youtube.com/embed/W3063iGJI_o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Configuring a LINE Official Account (OA) in Fox Connect**

---

### 1. Access Fox Connect and Initiate Channel Creation  
- Open **Fox Connect** → Navigate to **Settings**.  
- Select the **Channels** tab, then click **Add Channel**.  
- Choose **Connect Line OA account** as the channel type.  

> *All required fields must be populated for the booking system to function correctly.*

---

### 2. Enable Messaging API on LINE OA Manager  
- Go to the **LINE OA Manager** website and log in with your LINE credentials.  
- Click **Settings** → **Messaging API** (left‑hand menu).  
- Press **Enable Messaging API**.  
- In the popup, create a new provider:
  - Provide a name (any preferred label).  
  - Add URLs for **Privacy Policy** and **Terms of Use** (or skip if not ready).  
  - Confirm by clicking **OK**.  

> *Enabling the Messaging API is the first prerequisite for integration.*

---

### 3. Retrieve Credentials from LINE Developers Console  
| Item | How to obtain | Where to paste in Fox Connect |
|------|---------------|------------------------------|
| **Channel ID** | In the LINE Developers site, open your provider → select your OA account. Under **Basic settings**, copy the *Channel ID*. | Paste into the corresponding field in Fox Connect. |
| **Channel Secret** | Scroll down under **Basic settings**, copy the *Channel Secret*. | Paste into Fox Connect. |
| **Access Token** | Go to the **Messaging API** tab, scroll to the bottom and click **Issue**. Copy the generated token. | Paste into Fox Connect. |
| **Bot Basic ID** | At the top of the **Messaging API** tab, copy the *Bot Basic ID*. | Paste into Fox Connect. |

> *These credentials allow Fox Connect to authenticate and interact with the LINE Messaging API.*

---

### 4. Finalize Channel Setup in Fox Connect  
- After pasting all credentials, **Save** the configuration.  
- New fields should appear automatically (e.g., Webhook URL).  

---

### 5. Verify and Activate the Webhook  
- Return to the **Messaging API** tab in LINE Developers.  
- Locate the **Webhook URL** field and click **Verify** to ensure it is reachable.  
- Toggle **Use Webhook** to “On”.  

> *Enabling the webhook completes the channel setup, allowing real‑time message delivery.*

---

### Summary Checklist  

- [ ] Enabled Messaging API on LINE OA Manager.  
- [ ] Created a provider and recorded URLs (if applicable).  
- [ ] Copied **Channel ID**, **Channel Secret**, **Access Token**, and **Bot Basic ID**.  
- [ ] Pasted credentials into Fox Connect and saved.  
- [ ] Verified Webhook URL and enabled the webhook toggle.
