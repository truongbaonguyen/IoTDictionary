# **Trích xuất đặc trưng là gì?**
Trích xuất đặc trưng là một phần của quy trình giảm kích thước, trong đó, tập hợp dữ liệu thô ban đầu được chia và giảm thành các nhóm dễ quản lý hơn. Vì vậy, khi bạn muốn xử lý sẽ dễ dàng hơn. Đặc điểm quan trọng nhất của các tập dữ liệu lớn này là chúng có một số lượng lớn các biến. Các biến này yêu cầu nhiều tài nguyên máy tính để xử lý chúng. Vì vậy, việc trích xuất đặc trưng giúp có được tính năng tốt nhất từ ​​các tập dữ liệu lớn đó bằng cách chọn và kết hợp các biến thành các tính năng, do đó, giảm lượng dữ liệu một cách hiệu quả. Các tính năng này rất dễ xử lý, nhưng vẫn có thể mô tả tập dữ liệu thực tế với độ chính xác và độc đáo.
# **Tại sao trích xuất đặc trưng hữu ích?**
Kỹ thuật trích xuất các tính năng rất hữu ích khi bạn có một tập dữ liệu lớn và cần giảm số lượng tài nguyên mà không làm mất bất kỳ thông tin quan trọng hoặc liên quan nào. Tính năng trích xuất giúp giảm lượng dữ liệu dư thừa từ tập dữ liệu.

Cuối cùng, việc giảm dữ liệu sẽ giúp xây dựng mô hình với ít nỗ lực của máy hơn và cũng tăng tốc độ học và các bước tổng quát hóa trong quá trình máy học.
# **Làm thế nào để máy tính lưu trữ hình ảnh?**
Điều đầu tiên, chúng ta cần hiểu cách một máy có thể đọc và lưu trữ hình ảnh. Việc tải ảnh, đọc chúng rồi xử lý qua máy rất khó vì máy không có mắt như chúng ta.

Máy móc nhìn thấy bất kỳ hình ảnh nào dưới dạng ma trận số. Kích thước của ma trận này thực sự phụ thuộc vào số lượng pixel của hình ảnh đầu vào.

**Pixel là gì?**

Giá trị Pixel cho mỗi pixel là viết tắt hoặc mô tả độ sáng và màu sắc của pixel đó. Vì vậy, trong trường hợp đơn giản nhất của ảnh nhị phân, giá trị pixel là số 1 bit cho biết nền trước hoặc nền sau (ảnh trắng đen). Vậy pixel là số hoặc giá trị biểu thị cường độ hoặc độ sáng của pixel. Các số nhỏ gần 0 biểu thị màu đen và các số lớn gần 255 biểu thị màu trắng. Vậy, đây là khái niệm về pixel và cách máy nhìn thấy hình ảnh thông qua các con số mà không cần mắt.

![](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/08/article-image-16.png)

Tuy nhiên, đối với trường hợp hình ảnh có màu, chúng ta có 3 ma trận hoặc 3 kênh: màu đỏ (R), màu xanh lá (G), xanh lam (B). Trong 3 ma trận này, mỗi ma trận có các giá trị từ 0-255 đại diện cho cường độ màu của pixel đó.

![MATLAB | RGB image representation - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/Pixel.jpg)

Có thể thấy chúng ta cũng có 3 ma trận đại diện cho kênh RGB. Ba kênh này được xếp chồng lên nhau và được sử dụng để tạo thành một hình ảnh có màu. Đây là cách máy tính có thể phân biệt giữa các hình ảnh.

![](https://lh3.googleusercontent.com/AuDM9SFAk5-fvFf85dMu9xksW5cplbuIuYNlOYQATdO1XKkIOYpiGMHSWKffK6evT6Q9cAGmyPwBfIPTffcu2YodkjzRDYWbQvJLUoqHyyVRqlDTF2PQXDgUD63BWXydo5sOZq1qDdhpdgkvzewjb-vfNHAgDaZDyxbujGNQAc8nJ94PU6c11tmuVNnsZdYMIcHbUm5lPTplif-FjkqA_8q5PoLOlrl8c8d7ltarkto97V41HJKWz3y9Y0pP_6Wp145y0m4uo2YFJRCMM_likaFsewf6E4XO3ixP3jWeKkLOeN_nCzurKEIEOwPi00mHWl8BbkzkxrRrvv6RrwIraSJ-S8wHTEc2gDPAQ9H8gxmmGEaWELyE1QJJSIXE7fAuD61UdnE8S_BgyePYODdPH8lydOI_emm9LkcievEsZvhCxJ4zfa8qpk21bjpYngS2nTFDZYZReIesUBLZNdapl5KG-oaolkkRnd4_FjqzfTxST6fEN3wHYhBxFd0dq3hj0aodF4hzcWteUNQDQJm4jt1kR4rrbumyrYr94wUMuTFSQV3V5VnyJC2lnxbVR6-UCrrxu9RoGtigQksYq4a8MkDMkI0rmpOygb_jdIq1BFg0FPOhp0Q2KVt_IgJdvRXuR734PS5E0YMHQGSEQCwjTDk9kxEdATzrI6TlQJiSTG0bqm0bOn0lMuiPPFYX7FZjVeadpGhxKh4D3GNW_wEsWA=w991-h730-no?authuser=0)

![](https://lh3.googleusercontent.com/ZgSt-mZcnAygiW9vv8DbiegDkO8MdT3u2ZGhpgL-NM9YQMbM_sdMjI5Sj9Mg4118XzMx6bZk7zU8sxl-RcTQKNBg6ZxhYUjf4545wuC14VEi_gP1ypylEjgavPnVc45-4lVHS9QCoZ_4kcyImkxC0Q79T_2z4pGP7_KZ10f0lzV3wVU65leUvDefH-U8Tnv56BNzVwu9T-VpE82ZTlyqVpzGc35GA5k96QbIzE0y8yEP7aE1DIbsuqYSb5_jDglfRdRSfcU2LYxltvhy1tFYfFUZ7NH-pHgFY_75qCWoo7sfEISE3MlEdGSm4J-GLRnEhVMhD9z2ONlEAgGU4Fyfdk912JHE-KWgQ-BX-V4zfMuTSOxXl83po_2J-OZ9_VjIWZgkFKBhXpfpqxr97MbfssfDk-IvRF4_j2iBYtmHP91S7UTp2DmW-VeV3waq_zqn2ngLHOwOwlhKboP_H6ezRrPitp669S8_z5gjHu3ltV7pfEu2bKICIy6KwidKBQW9VZt5gxOvYIRLaTRWowWXNuw40r9Ka8azIkYR1qD8GDv9Ka12PjeTyW7GnmcpDWGqz2p82-piDvWQvcDZ1LeElvQjxRiYqMQ3KD7m5_rG43miPWDFqk9jl2LnnqHbPZ5YHawkz4LZaAZzVx70fEA_DKuBQHjs22tjLbechkoTEN0V1MHQ81T1-X4NdEiqr6GZZdGwNLw-u7gNg8YeC5H5Ag=w858-h715-no?authuser=0)



# **Cách sử dụng kỹ thuật trích xuất đặc trưng cho dữ liệu hình ảnh:**
## **Các đối tượng dưới dạng giá trị pixel thang độ xám**
Nếu chúng ta sử dụng ví dụ tương tự như hình ảnh mà chúng ta sử dụng ở trên tthì kích thước của hình ảnh là 340 x 680. Số lượng các đặc trưng giống như số lượng pixel nên số lượng đặc trưng sẽ là 340 x 680 = 231200.

Vì vậy, làm cách nào để khai báo 231200 pixel là các đặc trưng của hình ảnh này? Giải pháp là, chúng ta chỉ cần nối từng giá trị pixel lần lượt để tạo ra một vectơ đặc trưng cho hình ảnh.

`	`![](https://lh3.googleusercontent.com/rkBUhcvkwbrN7c9T0FIm_P2Svt7MrZHIBZa9LWD75jhb5PrDqDjGVmHKzIBwoOgzenJffHP6r8tsIm3EF3KHxY2uT3JHMmEQRN8S6n-cJ-pVd-UhcPL-p3ttSKYt7wbEYsFyCVPlDvGDuBfPlM_iSDRhSMchM5RjrIbVOhqUn6Xp8f_DS7KkRtETHhvg0gxoZnVxLb03HFImwMvzYt__veDW3_Tjp1wUkRBNinatCnK-Sktp50mImUUyDs5WnMQTu74f8gW2eo5iu8877UOUaVrzRqlYpYYgR5XkMORlOOB6xVu0fUvFjO6LUzk2OAyyKMDphDRFWzZPJLoE6kUoE26yLwHOgO8qGrd6AOarhTno3x7QUwyMZ5YtJWkV_7z9M9C7jR2S7eNkC07JekIn5-Bi4ppiRDy1OM46mih0uGNlnWtllCboBuzXcoB9mIV2qD1razLRcsgY_4IZPXReTFnaUp30S3-juTv1lKx56Yus_mV35d1Pp4xvA6pedy8VhyGi-DSlnCXznaT5W_4gIT4iRgpXpKoobFbC5uvqNAR4LYYJZQwrnCXWZwLltieln0e-xxIKT1feKHAXPB5kl97Pf-31AqOyOOoJVZ4i5_9pFjk3yqALjJq4J--fik-WzwwMFRl37uF2gAahlMGzgDE9KGqyKqwztfHA2F2K2iJsx1wX-zopQeQhDVSPvBmot8WGcngysP9ZTxYLYm5fkQ=w726-h672-no?authuser=0)
## **Giá trị pixel trung bình trong kênh**
![](https://lh3.googleusercontent.com/n9CHY78v-WLK-hPTVTiZiHgzOPyPSG-QmvEihVMXaqpQq2afnTrLoaHZejsKdWszx_7HZI9xITwDUrdW_ThZPLLtfs5DEhkpj30QLd6MldGUBZ7qxdd4C4oN2MXSKEv_7Tm4aEbsaUxHOum5FI8I1yWweRhU88eJ2_B6oRJd4l6dYkyRPtrbhRlvKjxkw71DXAKeJ8pngvEfqyuZw9Nb4xeozExZ1oucKTimZEoQ7rLLY_GwvKyCkC4gvSH-d-uyOqJKwd2RQCG2Su7Xfevrb64FjbVddFrvcEP49g6ybUMwmOu3dvKOoeaELvecjLStwdSFymNFziJlZpeEotJIpWmXJLd0fjWfYaSrbGzqzbcehwo_RTOiM_2qg2_jaZdDgIMaM8vUFbDjkkXTvNTGskh-l2ODfJsP9nzHRLNDu5eY0vogSwzxdsXPTRhfYN2BqU9ZoUN4gdK179kcRZdZppSa-OpDdeEjt0u0QQ1Auc89TC5qllG527KUlRcB3PVNJ6I_1E53wHI0usqUjISRRG5-c0TiAnyBeKiKMHnipH6_Yt9Vyp_axMicY9aUV_rFthF85FFnT-m0-akn3XABEfQUrsL42Gc6PcJ8aLtotm-Ss6n-4RmSmvQLH8kr6EEbcj1aOAoCGq4HPHNYTX5i6zNx5mm653Zg7wICjA1QvJTr9Rs5VSOQTP5HbtiQ_bGZG8l0gbTefFg0emY6WWz6dg=w894-h636-no?authuser=0)

Đối với trường hợp này, hình ảnh có một kích thước (340, 680, 3). Ba giá trị này đại diện cho giá trị RGB cũng như số lượng kênh. Bây giờ chúng ta sẽ sử dụng phương pháp trước để tạo các đặc trưng.

Tổng số đặc trưng của trường hợp này là 340\*680\*3 = 693600

![](https://lh3.googleusercontent.com/oQz62dnTEQ_LzLc5Agg9Ym_ocV1Yto0vfECnPvQAPYvGeNgCbvo_3HUFtMpGYNMSs85bVz9YPdxLV5motdl2WunvRzFXKQVQS8_q7J4opRvgRIZZaOt9ZRkoK9FT4rRzRnVR2tklUv98qKRnQ5bKXAVReO3jIPX-I1iLccY0RidmmTml33KPVudmCtjdpJjzMAHy5icTPIWmR87Gn82z6MTySq1RbCZ60GQKxmm9prqHFQTeGnCUVfFLU5rcoNOQoeJ6CVd2c1tUo-RHEdaUK0QaxL7p07gNgFFyqLcEmRMxb2l5atfhH7UEjufDDkhsDXzR6O96Cuwad3GP5GbeCVO0fMCpRypAZzBjFdKbbsvxeCUVNdnrqvph1Hbkh3SOVo3L0De0HLPvQnGOq2DOfnclefCsH9Vb12Tz6giXEoGGgQV2-JSSKeRuGtFQjx9e7T9XTepgY-HE8FjEVc8PJsouwtJB59pfpwP9VxzhDXFw6r6qwDfw_Oj-t-cn1HlUPSy281UXRevRUtldULreYUBAFjMeAs1bzEtrf-q00aIsxxYVCVKJTA48wwwJ6D3H3doc1WHMR7rDNO-TjtKhdmEuOxBtgJNnZz6y44FSyHTIHep3oHmUYkVAmO50mUf-LTqLGJdYClNzHhMeHudmgjOgS_FIl-mBSmAcwbyvr_dCdxYfYD_DbosHT79sBOfDpsH2ynW0WsLVmPsxtdXhdw=w839-h514-no?authuser=0)

Trong hình ảnh màu này có một ma trận 3D có kích thước (340 \* 680 \* 3) trong đó 340 biểu thị chiều cao, 680 là chiều rộng và 3 là số kênh. Để có được giá trị pixel trung bình cho hình ảnh, chúng ta sẽ sử dụng vòng lặp for.

![](https://lh3.googleusercontent.com/OWeKxVNYWM1B66sQRh5UEU0hFcQosEZiMqvoeNH_B41lMaAtetTxVmiFePkmBectQ7KlKLjXl5nQrpiALGdnQKQBX-DLL6ov5aTQBDgU3iW9-Ogu0CUbJqfiENope8ebHJNisd2mpsxym_JwTgnT6aW-rsmTgLUN_u4C5j56m1d4BvRV7qGgIFZETMDlaQEukpr-1sh_0YMaU9aPdQXNefTpZj-XHTw0qVbl46dzjQChgG0cTMxyvgQxxJzZPf5nitVcGIFXXGvNMR3icKCPr7hZM-bmk_gC9LgIatLz0Ot0KhALOHOpndN6Zmnx3awRoWFon42oCdqZG_qW7WA4T-r8yOcswStpAUVLHmJxO9dFu18W2PsMhge2UFVp95RQoBmpeYW11X7asl1SOiubYD5r4VvvT99G0igrWCJ0ILlBpqFJQ1NOHLHRyHfHUg5ViTTS8hDh-JMK66A8FprUwH24pbmwDiaMxcHq0OQ9FqnYEAkSXKd0XtZBYF9Hr_ByH8SAWE8NSdG3TEMocCpAJ234xnyvjplbCheq9f01xV0eG0yHgGussmPYHLbJxY8l-Kmy3WHhNKW2b5WbVoRABBCElnTg1nE33RPM74dmzAl5AimufAi-QKiUMBV77IyNE7MyzTsGYWY4NMNPuFGKn1qmblLGn6U704wF8FeF-tFMXpowf74n4nJQ2iU4mycssVOcCa-FY6pqH0RWFUOCcA=w995-h631-no?authuser=0)

Bây giờ chúng ta đã tạo ra một ma trận mới có cùng chiều cao và chiều rộng nhưng chỉ có 1 kênh. Để chuyển đổi ma trận thành mảng 1 chiều, chúng ta sẽ sử dụng thư viện Numpy như phần trước.

![](https://lh3.googleusercontent.com/XiUAhZIfTz9cFLI-NZJGDlAAReCbtd5MwOv8D-W1gsnvi6ljbFdlroTQCXEckWJs9Utba434yQlAfhgMFd4QWRL2pXoXMcw8ofjcdG6brFtkwJZoSmI0qB2WTYNm1s1l4tdTbjK9CIwu2cE9OyXahp5kipScioqgo2GwlySZD1Ru-B5ZKYl167PwrP5e8vJa1wulV3VDjhvW6h6ggGQiNDKO6RSWAzh8rIfq40S2sOXYCjA7XgvJO_l-9cH8Uz5yol_OiQ86SqdnmZZ4r_90cPDCJfYPIWyMRE6OcZwDq_5e6Vh_CBTX9jXVMt7rEl8Y8wWaiVYjwzmDhvYmF4OY_YUK9X53cgqmB5y263nLpxyU1yzCeKZgU8wjZjNWP36hwjmLD47apCdfoVOiJAmCfQWPMs8RzmzwaChvPpB55PlI9itkvZasr6Y-J_8oyXTyAanh8TtuFtFOnk7rRBriy7cESj7dNP6yePbxvROmXPk69uNsT8FeasO6qFGworCeZYXNiYJ9XB9svAraHXPSEpgAvU1T2UqmtCt4kjSKK0qJFp3aE77hWmbfASyKGGxqUa2TDwvT-vhbJCx5DsNPu5meBYLJ4RBWzJIzXGmv8mjnzQlHquLA6f5BSWKu0MUEdMgU7oGDhg98HJ7S7bWjsb1osYdi7ZbCO282r_Dq25NLtv5vBWKx_t4pYsLGobhpWRsI0Xl8oovoZ-xvquG2tg=w994-h440-no?authuser=0)
