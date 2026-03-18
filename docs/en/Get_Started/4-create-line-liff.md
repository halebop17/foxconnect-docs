---
icon: 
title: 4. Create LINE LIFF
---

# Create LINE LIFF

<iframe width="560" height="315" src="https://www.youtube.com/embed/Tbd2Hzno7Gc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Setting Up LINE LIFF Booking in Fox Connect**

---

### 1. Return to Channel Settings in Fox Connect  
- After completing the *Line OA* integration (see previous guide), navigate back to **Settings → Channels** in Fox Connect.  
- Scroll down until you find the **Line LIFF Booking** section; this is where the following details will be entered. 

---

### 2. Create a LINE Login Channel on the Developers Console  
1. Open the **LINE Developers** console (`https://developers.line.biz/console/`) and log in with your LINE account.  
2. From the provider list, select the provider you created earlier.
3. Click **Create New Channel**.  
4. In the popup, choose **LINE Login** as the channel type.  
5. Set the **Service Region** to *Thailand* and confirm the owner’s country (e.g., Thailand).  
6. Provide a **Channel Name** and **Description**.  
7. Check both **Web App** and **Mobile App** boxes.  
8. Agree to the LINE Developer Agreement and click **Create**. 

---

### 3. Configure the LIFF Tab  
1. Within the newly created channel, locate the **LIFF** tab and click **Add**.  
2. Enter a descriptive name for your LIFF app.  
3. Under **Size**, select **Full**.  
4. Copy the **Endpoint URL** from Fox Connect’s Line LIF ID for booking block (found in the channel settings).  
5. Paste this URL into the **Endpoint URL** field in the LIFF configuration.  
6. Tick all three checkboxes that appear below the URL and confirm the resulting pop‑up.  
7. For **Add Friend** option, set it to **On aggressive** (this enables the “Add friend” button automatically).  
8. Click **Add** to save the LIFF app configuration.  

---

### 4. Enable Share Target Picker & Publish  
1. On the next screen, toggle **Share Target Picker** to *On* and confirm the dialog that appears.  
2. At the top of the page, click the badge labeled **Developing** and confirm to publish the channel.  

---

### 5. Retrieve & Store the LIFF ID  
1. After publishing, a **LIFF ID** will appear at the bottom of the screen.  
2. Copy this ID and return to Fox Connect’s channel settings, pasting it into the **LIFF ID** field.  
3. Click **Save** to finalize the configuration.  

---

### 6. Completion  
Your LINE LIFF Booking integration is now fully configured and ready for use. You can proceed to the next section of the documentation or start testing the booking flow.

---