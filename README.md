# FarmCheatXkhang

## Giới thiệu

Đây là một công cụ giúp bạn dễ dàng tạo và lưu các script Lua.

## Cách sử dụng

1. **Truy cập trang web:** [Link đến trang web của bạn]
2. **Nhập script:** Dán code Lua của bạn vào ô nhập liệu.
3. **Lưu script:** Nhấn nút "Lưu" để lưu script vào một file Lua.
4. **Xem lại script:** Script đã lưu sẽ được hiển thị ở phần dưới.

## Tính năng

* Nhập và lưu script Lua một cách dễ dàng.
* Giao diện thân thiện với người dùng.

## **Lưu ý:**

* **Backend:** Bạn cần xây dựng một backend để xử lý việc lưu file. Có nhiều lựa chọn như:
    * **Firebase:** Cung cấp chức năng lưu trữ file và cơ sở dữ liệu.
    * **Node.js:** Với các framework như Express để tạo một server đơn giản.
    * **Python:** Với Flask hoặc Django.
* **Frontend:**
    * **HTML, CSS, JavaScript:** Để tạo một trang web cơ bản.
    * **Framework:** React, Vue, Angular... cho các ứng dụng phức tạp hơn.
* **GitHub:**
    * Sử dụng GitHub Pages để deploy trang web của bạn.

**Ví dụ code JavaScript đơn giản cho frontend:**
```javascript
const saveButton = document.getElementById('saveButton');
const codeInput = document.getElementById('codeInput');

saveButton.addEventListener('click', () => {
  // Gửi request đến backend để lưu file
  fetch('/save', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({ code: codeInput.value })
  })
  .then(response => response.json())
  .then(data => {
    console.log('File saved:', data);
  })
  .catch(error => {
    console.error('Error:', error);
  });
});
