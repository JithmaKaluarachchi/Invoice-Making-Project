# Invoice Studio

A small, dependency-free invoice generator based on the fields in the supplied invoice example. It runs entirely in the browser: calculations, draft saving, and PDF printing do not require a server or database.

## Run it locally

Open `index.html` in a browser. Enter your business and customer information, add invoice lines, and choose **Download / Print PDF**. In the print dialog, select **Save as PDF**.

The working draft is saved in browser storage on the current device and browser. The dashboard keeps saved invoices and archived invoice files in IndexedDB on this device. They are not backed up or synchronized, so keep PDF copies somewhere safe.

## Publish on Vercel

This is a static website, so it does not need a build command or server-side environment variables.

1. Push this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import that repository.
3. Keep the framework preset as **Other** (or no framework), leave the build command and output directory blank, and deploy.

Vercel's Hobby plan is for personal, non-commercial use. Check the current Vercel plan terms before using it for business invoicing or offering the app to customers. For commercial use, choose a hosting plan whose terms allow that use.

## Current scope

- Editable seller, customer, invoice, delivery, currency, and payment-note fields.
- Upload separate seller and customer logos for the invoice header and bill-to section.
- Add/remove line items with a delivery date and remarks per row; line totals and subtotal recalculate as you type.
- Optional fixed discount and tax percentage.
- Record a previous buyer advance and apply only the chosen amount to the current invoice; show the remaining advance and balance due.
- Attach up to two receipt images; they are compressed in the browser and printed on a supporting-receipts page.
- Optional signature image, thank-you message, and dated signature area at the end of the invoice.
- Browser-local draft persistence.
- A home dashboard with invoice and advance summaries, created and uploaded invoice cards, date sorting, search, and delete/open controls.
- A dashboard popup for uploading previous invoice PDFs and images; saved files are dated and displayed as cards with the created invoices.
- Responsive live preview and print-to-PDF layout.

There is no login, cloud sync, database, email sending, or automatic invoice-number sequence yet.
