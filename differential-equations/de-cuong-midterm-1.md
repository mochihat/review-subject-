# Đề cương ôn Midterm I – Phương trình vi phân

Môn Differential Equations (微分方程) – Jerry Tai (戴立嘉), NYCU, Fall 2026. Cập nhật 2026-10-03.

## Phạm vi thi và thông tin chung

Midterm I chiếm 25% điểm, gồm dưới 30 câu trắc nghiệm. Phạm vi thi là toàn bộ Lecture 1–10: phương trình bậc nhất (Lecture 2–7) và phương trình bậc hai hệ số hằng (Lecture 8–10).

- Ngày thi: cần xem thông báo trên E3 (e3.nycu.edu.tw).
- Không có homework. Thầy nói một số câu thi có thể lấy từ giáo trình Nagle, Saff, Snider (bản 9), nên hãy luyện bài tập cuối mỗi mục tương ứng.
- Vắng Midterm I có lý do chính đáng thì Midterm II tính 50%.
- Final thi toàn bộ môn, nên kiến thức Midterm I sẽ gặp lại.
- Thư mục Downloads/1232/Lecture1 có bài tập separable, exact và linear từ năm 2019. File đề có mật khẩu, nhưng 2 file lời giải (exact, separable) mở được.

## Checklist chủ đề

Ưu tiên cao nhất là các kỹ năng giải: tách biến, thừa số tích phân, exact, bể muối và phương trình bậc hai hệ số hằng. Tích vào khi bạn tự giải được mà không nhìn lời giải.

**Ưu tiên cao (gần như chắc chắn ra thi)**

- [ ] Phân loại phương trình: ODE/PDE, bậc, tuyến tính hay không (L2)
- [ ] Giải phương trình tách biến, cả nghiệm tổng quát và bài toán giá trị đầu (L4)
- [ ] Giải phương trình tuyến tính bậc nhất bằng thừa số tích phân, kèm tích phân từng phần (L5)
- [ ] Kiểm tra exact và tìm ψ(x, y) (L6)
- [ ] Chọn đúng phương pháp khi đề không nói dùng cách nào (L4–6)
- [ ] Dựng và giải bài toán bể muối, tìm giới hạn và thời gian T (L7)

**Ưu tiên trung bình**

- [ ] Tìm điểm cân bằng, xét ổn định, bảng hành vi khi t → ∞ theo y(0) (L3)
- [ ] Phác họa trường hướng và đường cong tích phân (L3, L4)
- [ ] Hành vi dài hạn của nghiệm tuyến tính bằng giới hạn (L5)
- [ ] Lãi kép liên tục có gửi thêm hoặc rút tiền (L7)

**Ưu tiên cao: bậc hai**

- [ ] Phương trình đặc trưng, nghiệm thực phân biệt và 2 điều kiện đầu (L8)
- [ ] Nghiệm phức và công thức Euler (L9)
- [ ] Nghiệm kép, giảm bậc, Wronskian (L10)

## Quy trình giải từng dạng

Gặp một phương trình bậc nhất, đầu tiên kiểm tra tách biến, tiếp theo là tuyến tính, cuối cùng là exact. Sau đó làm đúng các bước của dạng tìm được.

**Dạng 1: Tách biến**, y' = f(x) g(y)

1. Ghi lại nghiệm hằng: mọi y\* có g(y\*) = 0.
2. Chia cho g(y): dy / g(y) = f(x) dx.
3. Tích phân hai vế, chỉ cộng một hằng số C.
4. Thay điều kiện đầu để tìm C, rồi giải ra y nếu được. Chọn dấu ± cho khớp với điều kiện đầu.

**Dạng 2: Tuyến tính**, a(t) y' + b(t) y = c(t)

1. Chia cho a(t) để được y' + p(t) y = g(t). Bước này hay bị quên.
2. Tính μ = e^(∫p dt). Ví dụ p = 2/t thì μ = e^(2 ln t) = t².
3. Viết (μy)' = μg.
4. Tích phân: μy = ∫μg dt + C. Phải có C trước khi chia cho μ.
5. y = (∫μg dt + C) / μ, thay điều kiện đầu, rồi xét t → ∞ nếu đề hỏi.

**Dạng 3: Exact**, M(x, y) + N(x, y) y' = 0

1. Xác định M và N, tính M_y và N_x. Hai đạo hàm phải bằng nhau.
2. ψ = ∫M dx + h(y).
3. ψ_y = N, từ đó suy ra h'(y). h'(y) chỉ được chứa y; nếu còn x thì đã tính sai.
4. Nghiệm ψ(x, y) = C, thay điều kiện đầu để tìm C.

**Dạng 4: Cân bằng và ổn định**, y' = f(y)

1. Giải f(y) = 0 để có các giá trị cân bằng, sắp xếp trên trục y.
2. Xét dấu f trong từng khoảng (thử một điểm bất kỳ).
3. Mũi tên hai bên cùng hướng vào thì ổn định. Cùng hướng ra thì không ổn định. Một vào một ra thì bán ổn định.
4. Lập bảng "y(0) trong khoảng nào thì y → đâu".

**Dạng 5: Bể trộn (mixing)**

1. Đặt Q(t) là lượng chất tan, không phải nồng độ.
2. Q' = (nồng độ vào × lưu lượng vào) − (Q / V(t) × lưu lượng ra), với V(t) = V₀ + (vào − ra) t.
3. Giải bằng thừa số tích phân (hoặc tách biến nếu V không đổi).
4. Giới hạn Q_L = nồng độ vào × V khi V không đổi. Dùng logarit để tìm thời gian T.

**Dạng 6: ay'' + by' + cy = 0**

1. Viết ar² + br + c = 0 và tính Δ = b² − 4ac.
2. Δ > 0 cho c₁e^(r₁t) + c₂e^(r₂t). Δ < 0 cho e^(λt)(c₁ cos μt + c₂ sin μt). Δ = 0 cho (c₁ + c₂t)e^(rt).
3. Tính y' rồi thay y(t₀), y'(t₀) để giải hệ tìm c₁, c₂.

## Bài tập luyện tập

Có 12 bài theo thứ tự các dạng ở trên, do mình tự soạn. Hãy tự giải trước rồi mới xem đáp án. Mọi đáp án đã được thử lại vào phương trình.

**Phân loại (L2)**

1. Phân loại theo bậc, tuyến tính, ODE/PDE: (a) t²y'' + ty' + 2y = sin t; (b) y' = y² + t; (c) y''' + y y' = 0; (d) u_t = u_xx + u.
   - Đáp án: (a) bậc 2 tuyến tính ODE; (b) bậc 1 phi tuyến ODE; (c) bậc 3 phi tuyến ODE (vì có tích y·y'); (d) bậc 2 tuyến tính PDE.

**Tách biến (L4)**

2. y' = x² / y, y(0) = −2.
   - Đáp án: y² = 2x³/3 + 4. Vì y(0) < 0 nên y = −√(2x³/3 + 4).
3. y' = (1 + y²) e^x, y(0) = 1.
   - Đáp án: arctan y = e^x + C, với C = π/4 − 1. Suy ra y = tan(e^x + π/4 − 1).

**Tuyến tính (L5)**

4. t y' + 2y = 4t², y(1) = 2, t > 0.
   - Đáp án: chia cho t được y' + (2/t) y = 4t, μ = t². Khi đó (t²y)' = 4t³, nên y = t² + C/t² với C = 1. Vậy y = t² + 1/t².
5. y' + y = t, y(0) = 0. Tìm thêm hành vi khi t → ∞.
   - Đáp án: μ = e^t, (e^t y)' = t e^t. Tích phân từng phần cho e^t y = (t − 1)e^t + C, nên y = t − 1 + e^(−t). Khi t → ∞, y ≈ t − 1 (tiệm cận xiên).

**Exact (L6)**

6. (y cos x + 2x e^y) + (sin x + x² e^y − 1) y' = 0.
   - Đáp án: M_y = N_x = cos x + 2x e^y nên phương trình exact. ψ = y sin x + x² e^y + h(y), h'(y) = −1. Nghiệm: y sin x + x² e^y − y = C.
7. (3xy + y²) + (x² + xy) y' = 0 có exact không?
   - Đáp án: không, vì M_y = 3x + 2y nhưng N_x = 2x + y.

**Cân bằng và ổn định (L3)**

8. y' = y² − 4y + 3. Tìm cân bằng, xét ổn định, mô tả y khi t → ∞ theo y(0).
   - Đáp án: y' = (y − 1)(y − 3). y = 1 ổn định, y = 3 không ổn định. Nếu y(0) < 3 thì y → 1; y(0) = 3 thì y = 3; y(0) > 3 thì y → ∞.

**Mô hình (L7)**

9. Bể 200 L nước sạch. Nước muối 2 g/L chảy vào 5 L/min, hỗn hợp chảy ra 5 L/min. Tìm Q(t), Q_L, và thời điểm Q = 200 g.
   - Đáp án: Q' = 10 − Q/40, Q(0) = 0. Suy ra Q = 400(1 − e^(−t/40)), Q_L = 400 g, và t = 40 ln 2 ≈ 27.7 phút.

**Bậc hai (L8–10)**

10. y'' − y' − 6y = 0, y(0) = 1, y'(0) = 8.
    - Đáp án: r = 3, −2. y = 2e^(3t) − e^(−2t).
11. y'' + 4y = 0, y(0) = 2, y'(0) = 6.
    - Đáp án: r = ±2i. y = 2 cos 2t + 3 sin 2t.
12. y'' − 6y' + 9y = 0, y(0) = 1, y'(0) = 5.
    - Đáp án: nghiệm kép r = 3. y = (1 + 2t) e^(3t).

## Bài tập trong sách cần làm

Làm theo thứ tự ưu tiên dưới đây, dùng sách Zill & Cullen, *Differential Equations with Boundary-Value Problems* (file đã có trong Downloads). Mức 1 và mức 2 đều bắt buộc, tổng 81 bài, mỗi bài khoảng 3–5 phút, tổng cộng khoảng 5–6 giờ.

Thầy dùng sách Nagle–Saff–Snider nhưng máy bạn không có cuốn đó. Zill có cùng các dạng bài, nên dùng thay được. Mình chọn chủ yếu bài số lẻ vì đáp án có ở cuối sách (từ trang ANS-1), để bạn tự kiểm tra.

**Mức 1: bắt buộc, bậc nhất (Lecture 2–7)**

| Mục trong Zill | Trang | Bài | Lecture | Dạng |
| --- | --- | --- | --- | --- |
| 1.1 Definitions and Terminology | 10 | 1, 3, 5, 7 | L2 | Phân loại bậc, tuyến tính |
| 1.1 | 10 | 11, 13, 15 | L2 | Kiểm tra một hàm có phải là nghiệm |
| 1.1 | 10 | 27, 29, 31 | L2, L8 | Tìm m để y = e^(mx) hoặc x^m là nghiệm |
| 1.1 | 10 | 33, 35 | L3 | Tìm nghiệm hằng |
| 2.1 Solution Curves Without a Solution | 41 | 13 | L3 | Đọc trường hướng từ hình |
| 2.1 | 41 | 21, 23, 25, 27 | L3 | Điểm tới hạn, xét ổn định |
| 2.2 Separable Variables | 50 | 1, 3, 5, 7, 9, 11, 13, 15 | L4 | Nghiệm tổng quát |
| 2.2 | 50 | 23, 25 | L4 | Bài toán giá trị đầu |
| 2.3 Linear Equations | 60 | 1, 3, 5, 7, 9, 11, 13, 15 | L5 | Nghiệm tổng quát |
| 2.3 | 60 | 25, 27 | L5 | Bài toán giá trị đầu |
| 2.4 Exact Equations | 68 | 1, 3, 5, 7, 9, 11 | L6 | Kiểm tra exact và giải |
| 2.4 | 68 | 21, 23 | L6 | Bài toán giá trị đầu |
| 2.4 | 68 | 27 | L6 | Tìm k để phương trình exact |
| 3.1 Linear Models | 89 | 21, 22, 23, 24, 25 | L7 | Bể trộn (mixture) |
| 3.1 | 89 | 10 | L7 | Lãi kép liên tục |
| Chapter 2 in Review | 80 | 1, 2, 3, 4 | L3–6 | Câu hỏi khái niệm, điền nhanh |
| Chapter 2 in Review | 80 | 11, 13, 15, 17, 19 | L4–6 | Bài trộn lẫn, phải tự nhận ra dạng |

**Mức 2: bắt buộc, bậc hai (Lecture 8–10)**

| Mục trong Zill | Trang | Bài | Lecture | Dạng |
| --- | --- | --- | --- | --- |
| 4.3 Homogeneous Linear Equations with Constant Coefficients | 138 | 1, 3, 5, 7, 9, 11, 13 | L8–10 | Nghiệm tổng quát, đủ 3 trường hợp Δ |
| 4.3 | 138 | 29, 31, 33 | L8–10 | Bài toán giá trị đầu |
| 4.3 | 138 | 43–48 | L8–10 | Ghép phương trình với đồ thị nghiệm, rất giống câu trắc nghiệm |
| 4.2 Reduction of Order | 132 | 1, 3, 5, 7 | L10 | Giảm bậc khi biết một nghiệm |

**Mức 3: nếu còn thời gian**

- Zill 2.2, 2.3, 2.4: các bài số lẻ còn lại trong phần nghiệm tổng quát.
- Sách Edwards & Penney (cũng có trong Downloads) để đổi gió: mục 1.3 (trường hướng), 1.4 (tách biến), 1.5 (tuyến tính), 1.6 (exact, phần cuối mục), 2.3 (bậc hai hệ số hằng).

**Mẹo cho đề trắc nghiệm dưới 30 câu:** bình quân mỗi câu chỉ có vài phút, nên không phải câu nào cũng cần giải trọn vẹn.

- Thử đáp án ngược: thay từng đáp án vào phương trình, thường nhanh hơn giải từ đầu.
- Có điều kiện đầu thì thay t = t₀ vào các đáp án trước. Thường loại được 2–3 đáp án ngay.
- Câu ổn định chỉ cần xét dấu f(y), không cần giải phương trình.
- Câu exact chỉ cần so M_y với N_x. Câu "tìm k" thì cho hai đạo hàm bằng nhau rồi giải ra k.
- Câu bậc hai: từ Δ biết ngay dạng nghiệm (e mũ, cos/sin, hay t·e mũ) và loại được đáp án sai dạng.
- Câu giới hạn t → ∞: cho số hạng mũ âm bằng 0, rồi kiểm tra bằng ý nghĩa vật lý (ví dụ bể muối: nồng độ vào × thể tích).

## Lỗi thường gặp và mẹo làm bài

Phần lớn điểm bị mất ở các bước đại số, ít khi do sai phương pháp.

| Lỗi | Cách tránh |
| --- | --- |
| Quên chia hệ số của y' trước khi tính μ | Luôn viết lại dạng chuẩn y' + p y = g trước |
| Thêm C sau khi đã chia cho μ (thành y = … + C) | Cộng C ngay sau khi tích phân, rồi mới chia |
| Mất nghiệm hằng khi chia cho g(y) | Giải g(y) = 0 và ghi các nghiệm đó trước |
| Sai dấu ± khi khai căn | Chọn dấu theo điều kiện đầu |
| Đạo hàm riêng sai khi kiểm tra exact | Khi tính M_y thì coi x là hằng số, và ngược lại |
| h'(y) còn chứa x | Dấu hiệu tính sai hoặc phương trình không exact; tính lại |
| Bể trộn: dùng nồng độ thay cho lượng | Q là lượng; lượng ra = (Q/V) × lưu lượng ra |
| Bậc hai: thay điều kiện y'(0) vào y thay vì y' | Tính y' đầy đủ, đặc biệt với t e^(rt) và e^(λt) cos μt |

**Mẹo:**

- Làm xong thì thử lại: thay y vào phương trình và điều kiện đầu, chỉ mất khoảng 1 phút.
- Nhớ các tích phân hay gặp: ∫t e^t dt = (t − 1)e^t, ∫dy/(1 + y²) = arctan y, ∫dy/y = ln|y|, e^(k ln t) = t^k.
- Đề hỏi "behavior as t → ∞" thì ghi rõ giới hạn và nó phụ thuộc y(0) thế nào.
- Nghiệm ẩn ψ(x, y) = C là đáp án hợp lệ, không cần cố giải ra y.

## Kế hoạch ôn 7 ngày

Mỗi ngày một dạng bài, khoảng 1.5–2 giờ. Ngày 7 là ngày sát kỳ thi. Nếu còn ít ngày hơn thì gộp ngày 1 với 2. Không nên cắt ngày 6, vì bậc hai chiếm 3/10 lecture.

- [ ] Ngày 1: Lecture 2–3. Phân loại, trường hướng, cân bằng và ổn định. Làm bài 1, 8 và ví dụ y' = (y² − y − 2)(1 − y)² trong slide.
- [ ] Ngày 2: Lecture 4. Tách biến. Làm bài 2, 3 và 5–6 bài trong sách.
- [ ] Ngày 3: Lecture 5. Thừa số tích phân và ôn tích phân từng phần. Làm bài 4, 5 và 5–6 bài trong sách.
- [ ] Ngày 4: Lecture 6. Exact. Làm bài 6, 7 và 5–6 bài trong sách.
- [ ] Ngày 5: Lecture 7. Bể muối và lãi kép. Làm lại toàn bộ ví dụ bể muối (a)–(e) trong slide và bài 9.
- [ ] Ngày 6: Lecture 8–10. Phương trình đặc trưng, nghiệm phức, nghiệm kép, giảm bậc. Làm bài 10–12 và mức 2 trong sách (Zill 4.2, 4.3).
- [ ] Ngày 7: Tự thi thử 90 phút với 6–8 bài trộn lẫn, không ghi dạng bài. Sau đó xem lại bảng lỗi thường gặp.
