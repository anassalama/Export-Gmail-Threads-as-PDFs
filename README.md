# 📧 Export Gmail Threads as PDFs

This Google Apps Script project allows users to **export Gmail threads as PDF files** and save them to a specified Google Drive folder. It also supports searching and filtering Gmail threads based on specific queries.

---

## 🚀 **Features**

- Export selected Gmail threads as PDF files.
- Support for exporting email content, including images and attachments.
- Option to merge multiple email threads into a single PDF.
- Save PDFs directly to a designated Google Drive folder.
- Search Gmail threads using a custom query and preview results in a Google Sheet.
- Track the export status in the Google Sheet.

---

## 📋 **Setup Instructions**

### 1. **Google Sheet Configuration**
- Create a Google Sheet with the following **named ranges:**
   - `query`: Gmail search query.
   - `max`: Maximum number of threads to fetch.
   - `printMessagesOnly`: Boolean value to print only message content.
   - `filename`: Custom filename for the exported PDF.
   - `folder`: Google Drive folder ID for saving PDFs.
   - `status`: Export status (Success/Error/Warning).
   - `message`: Detailed export message.
   - `tableThreads`: Starting cell for thread results.
   - `merge`: Boolean value to merge all threads into a single PDF.

### 2. **Enable Gmail & Drive APIs**
- Go to **Google Cloud Console**.
- Enable the following APIs:
   - **Gmail API**
   - **Google Drive API**

### 3. **Add Google Apps Script**
- Open the Google Sheet.
- Go to **Extensions > Apps Script**.
- Copy and paste the script provided in the code editor.

### 4. **Authorize Script**
- Save the script.
- Run `onSearch` and `onPrint` functions manually to authorize the script.

---

## 🛠️ **How to Use**

### **1. Search Gmail Threads**
- Fill in the `query` and `max` fields in the Google Sheet.
- Click the **Search** button.
- Matching Gmail threads will populate in the thread table.

### **2. Export Gmail Threads**
- Select the threads you want to export in the `Select` column.
- Choose a folder ID and filename.
- Click the **Print** button.

### **3. Merge Threads (Optional)**
- Enable the `merge` option to combine all threads into a single PDF.

### **4. View Status**
- Check the `status` and `message` fields for success or error messages.

---

## 🧩 **Key Functions**

- `onSearch`: Searches Gmail based on the query and displays results.
- `onPrint`: Exports selected threads as PDFs and saves them in Google Drive.
- `createThreadContent_`: Processes email content and embeds images.
- `htmlToPdf_`: Converts HTML email content into a PDF.
- `_updateStatus_`: Updates status and messages in the Google Sheet.

---

## ⚠️ **Troubleshooting**

- Ensure the APIs are enabled in the Google Cloud Console.
- Verify that the folder ID is correct.
- Check logs in **View > Executions** in the Apps Script editor.
- If encountering errors with image URLs, ensure invalid URLs are filtered out.

---

## 📚 **Dependencies**

- **GmailApp**: To fetch Gmail threads and messages.
- **DriveApp**: To save PDF files to Google Drive.
- **SpreadsheetApp**: To interact with Google Sheets.
- **UrlFetchApp**: To fetch external images embedded in emails.

---

## 🤝 **Contributing**
Feel free to suggest improvements or report bugs.

---

## 📜 **License**
This project is licensed under the **MIT License**.

---

## 📞 **Support**
For support or queries, contact the project maintainer.

**Happy Automating! 🚀**

