# 🧪 Cross-Browser and Cross-Device Testing Report

## 🔗 Website Under Test
[https://shoplane-by-lassie.netlify.app/](https://shoplane-by-lassie.netlify.app/)

---

## ✅ Test Summary

| Test Parameter     | Values Tested                                                                 |
|--------------------|-------------------------------------------------------------------------------|
| Browsers           | Google Chrome (v125), Mozilla Firefox (v126), Microsoft Edge (v125), Safari (iOS 17) |
| Devices            | Desktop (1920×1080), Tablet (768×1024), Mobile (360×800)                     |
| OS Used            | Windows 11, macOS Ventura, Android 13, iOS 17                                 |
| Testing Tools Used | Manual inspection + DevTools (Responsive Mode)                                |

---

## 🔍 Test Scenarios & Observations

### 1. **Homepage Layout**

| Device     | Browser      | Status         | Issues Found                                                                 |
|------------|--------------|----------------|-------------------------------------------------------------------------------|
| Desktop    | All          | ✅ OK          | Layout consistent across all browsers                                        |
| Tablet     | Chrome/Edge  | ✅ OK          | Slight overflow of product cards on some zoom levels                         |
| Mobile     | Firefox      | ⚠️ Minor Issue | Navbar overlaps product text; spacing needs improvement                      |
| Mobile     | Safari       | ❌ Broken View | Hero image does not scale properly; text cuts off at edges                   |

### 2. **Navigation Menu & Links**

| Device     | Browser      | Status         | Issues Found                                                                 |
|------------|--------------|----------------|-------------------------------------------------------------------------------|
| All        | Chrome/Edge  | ✅ OK          | All links functional                                                         |
| Mobile     | Firefox      | ✅ OK          | Links work, but touch areas are too small for finger-based interaction       |
| Mobile     | Safari       | ⚠️ Broken Link | "Contact Us" in footer doesn't work (taps but no action)                     |

### 3. **Product Page Functionality**

| Device     | Browser      | Status         | Issues Found                                                                 |
|------------|--------------|----------------|-------------------------------------------------------------------------------|
| Desktop    | All          | ✅ OK          | Add to cart, details view all working properly                              |
| Mobile     | Safari       | ❌ Broken CSS  | Buttons not visible below fold; layout broken                                |
| Tablet     | Firefox      | ⚠️ Minor Issue | Product image zoom not functioning consistently                              |

---

## 🧾 Summary of Issues Found

| Severity | Issue Description                                                   | Affected Browser(s)/Device(s)      | Recommended Fix                         |
|----------|----------------------------------------------------------------------|------------------------------------|------------------------------------------|
| High     | Hero image scaling/cropping                                         | Safari on iOS                      | Use `object-fit: cover` and `media queries` for iOS safari fix |
| Medium   | Footer "Contact Us" link unresponsive                               | Safari on iOS                      | Add `href` or JS fallback for mobile     |
| Medium   | Navbar overlap on product text                                      | Firefox on small screens           | Add `z-index` and spacing adjustments    |
| Low      | Touch targets too small                                             | Mobile Firefox                     | Use `min-width` and `padding` on links   |
| Low      | Slight card overflow on tablet in zoom mode                         | Chrome/Edge                        | Add `max-width` and `overflow: hidden`   |

---

## ✅ Recommendations

- Use a **responsive framework** like Bootstrap or Tailwind for layout handling.
- Run **Safari-focused QA** due to common mobile Safari issues.
- Use tools like **BrowserStack** or **Lambdatest** for device simulation testing.
- Validate all links with automated link checker (e.g., W3C Link Checker).
- Ensure **touch targets** are WCAG-compliant (`44px × 44px` minimum).

---

## 🧑‍💻 Tester Info

- **Name:** Varun Girish Deshmukh  
- **Internship Track:** Software Testing  
- **Task Number:** 02  
