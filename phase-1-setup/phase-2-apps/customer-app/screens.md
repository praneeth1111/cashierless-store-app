# 🎨 Power Apps – Customer App Screens

This file documents the screen designs used in the cashierless store customer-facing app (Canvas App).

---

## 🧾 Screen 1: Entry QR Scanner

| Element  | Type     | Name           |
|----------|----------|----------------|
| Camera   | Control  | camQRScanner   |
| Label    | Text     | lblInstructions |
| Logic    | Formula  | If(ScanData.Text = "STORE_ENTRY_QR", Navigate(FeedbackScreen), Notify("Invalid QR", Error)) |

---

## 📝 Screen 2: Feedback Form

| Element       | Type         | Name              |
|---------------|--------------|-------------------|
| Rating        | Star control | ratingFeedback    |
| Text input    | Text         | txtComments       |
| Camera        | Control      | camPhotoUpload    |
| Submit Button | Button       | btnSubmit         |

**Submit logic:**
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

---

## 🤖 Screen 3: AI Recommendations

| Element       | Type     | Name               |
|---------------|----------|--------------------|
| Gallery       | Gallery  | galRecommendations |
| Add to Cart   | Button   | btnAddToCartA      |

**Gallery items logic:**
```powerapps
Filter(
  Products,
  Category in First(AIRecommendations.User(User().Email)).Categories
)

