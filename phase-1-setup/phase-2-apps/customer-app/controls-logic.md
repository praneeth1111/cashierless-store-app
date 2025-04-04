# ⚙️ Power Apps – Controls & Logic

This file documents the key formulas and logic used across the customer app screens.

---

## 📸 QR Scanner Logic

**camQRScanner.OnScan:**
```powerapps
If(
  ScanData.Text = "STORE_ENTRY_QR",
  Navigate(FeedbackScreen, Fade),
  Notify("Invalid QR code", Error)
)

---

## 📝 Feedback Submission

**btnSubmit.OnSelect:**
```powerapps
Patch(
  Feedback,
  Defaults(Feedback),
  {
    Rating: ratingFeedback.Value,
    Comments: txtComments.Text,
    Image: camPhotoUpload.Photo
  }
);
Notify("Feedback Submitted!", Success)


Filter(
  Products,
  Category in First(AIRecommendations.User(User().Email)).Categories
)

Collect(
  Cart,
  ThisItem
);
Notify("Item added to cart", NotificationType.Success)


