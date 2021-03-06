---
title: "Học Khoa học máy tính nên đọc sách gì?"
date: 2020-09-02T20:46:47+07:00
categories: [book]
tags: [book,khmt,cs]
---

Note lại từ nguồn: https://procul.org/blog/2007/10/01/sach-khmt/

Bạn trantempo hỏi một danh sách các sách nên đọc trong KHMT. Bạn Nguyên đã đưa một danh sách sơ bộ. Tôi sẽ cập nhật từ từ vào danh sách dưới đây trong một vài tuần tới để có một danh sách hoàn tất hơn. (Cần về nhà duyệt lại tủ sách). Các bạn có thể bình luận và thêm vào các quyển sách mà bạn ưa thích.

- Phân tích thiết kế thuật toán cơ bản
- Phân tích thiết kế thuật toán nâng cao
- Combinatorics (bao gồm lý thuyết đồ thị và toán rời rạc)
- Xử lý ngôn ngữ tự nhiên (danh sách của anh Bạch Hưng Nguyên)
- Machine learning và statistics (danh sách của anh Nguyễn Xuân Long)
- Databases (anh Đoàn An Hải giới thiệu)

## 1. Phân tích và thiết kế thuật toán (cơ bản)

Hiện nay có 3 quyển textbooks được dùng khá phổ biến, trong đó tôi thích quyển của Kleinberg và Tardos nhất. Tuy nhiên, từ quan điểm cá nhân thì tôi chưa thấy hài lòng với cả 3 vì các lý do khác nhau, mặc dù cả ba quyển đều rất tốt.

- Thomas H. Cormen, Charles E. Leiserson, Ronald Rivest, and Clifford Stein, **Introduction to Algorithms (2e)**, 1180pp, ISBN: 0262032937, MIT Press, September 2001.
- Jon Kleinberg, Éva Tardos, **Algorithm Design** , 864 pages, Addison Wesley, ISBN-10: 0321295358, ISBN-13: 978-0321295354, March 16, 2005.
- S. Dasgupta, C.H. Papadimitriou, and U.V. Vazirani, ** Algorithms**, McGraw Hill, 2007.

Hồi trước có quyển của Aho-Hopcroft-Ullman. Bây giờ đã khá lỗi thời, ít ai dùng.

- Alfred V. Aho John E. Hopcroft Jeffrey Ullman, Data Structures and Algorithms, 427pp. ISBN: 0201000237, Addison Wesley, January 1983.

Tiếc rằng Robert Tarjan không viết sách giáo khoa, nếu không sách về data structure của ông hẳn phải rất hay.

Hiện nay không thể dạy thuật toán cơ bản mà không dạy về NP-Completeness và các phương pháp xác suất. Do đó, các quyển sau đây cũng rất cần thiết:

- Michael R. Garey and David S. Johnson, Computers and Intractability: A Guide to the Theory of NP-Completeness, 338pp. ISBN: 0716710455, W. H. Freeman Company, November 1990.
- Michael Mitzenmacher and Eli Upfal, Probability and Computing: Randomized Algorithms and Probabilistic Analysis, Cambridge University Press (January 31, 2005)
Tôi xếp 3 tập của Knuth vào dạng “cao cấp hơn”, trong trường hợp bạn đang thắc mắc. Về lecture notes (dạng presentation) thì tôi thấy notes của … tôi khá tốt 🙂 (từ từ đến cuối học kỳ sẽ có toàn bộ notes.)

## 2. Phân tích và thiết kế thuật toán (cao cấp hơn)

Khi nói đến phân tích và thiết kế thuật toán cao cấp, ta thường phải xem xét các đề tài cụ thể để giới thiệu. Các quyển sách cao cấp thường được viết về một đề tài nào đó: approximation algorithms, randomized algorithms, linear programming, convex programming, approximate counting, combinatorial optimization, network flows, algorithmic game theory, vân vân. Tôi sẽ gộp chung chúng lại và giới thiệu một vài quyển tiêu biểu.

- Donald Knuth, **The Art of Computer Programming** Volumes 1, 2, 3, Addison Wesley.
- Vijay Vazirani, Approximation Algorithms, Springer-Verlag, 397 pages hardcover, ISBN: 3-540-65367-8, published 2001.
- Rajeev Motwani and Prabhakar Raghavan, Randomized Algorithms, 492 pages, Cambridge University Press (August 25, 1995), ISBN: 0521474655
- Vašek Chvátal, Linear Programming, W. H. Freeman, 1983; 478pp. ISBN: 0716715872, W. H. Freeman Company, January 1983.
- Dorit Hochbaum (Editor), Approximation Algorithms for NP-Hard Problems, 624 pages ; Brooks/Cole Pub Co; ISBN: 0534949681; 1st edition (July 26, 1996)
- Alexander Schrijver, Theory of Linear and Integer Programming, 484pp. ISBN: 0471982326, Wiley, John & Sons, Incorporated, June 1998.
- Christos H. Papadimitriou and Kenneth Steiglitz, Combinatorial Optimization: Algorithms and Complexity, Dover Publications; Unabridged edition (January 29, 1998).
- Mark Jerrum, Counting, Sampling and Integrating: Algorithms and Complexity (Lectures in Mathematics. ETH Zürich), Birkhäuser Basel; 1 edition (April 28, 2003)
- Ravindra K. Ahuja, Thomas L. Magnanti, and James B. Orlin, Network Flows: Theory, Algorithms, and Applications, Hardcover, 1st ed., 846pp., ISBN: 013617549X, Prentice Hall, February 1993.
- Noam Nisan, Tim Roughgarden, Eva Tardos, and Vijay V. Vazirani (editors), Algorithmic Game Theory, Cambridge University Press, 2007.
- Mark de Berg, M. van Krefeld, M. Overmars, and O. Schwarzkopf, Computational Geometry: Algorithms and Applications, Second Edition, Springer; 2nd rev. ed. edition (February 18, 2000).

Đây là tôi hoàn toàn chưa đụng tới rất nhiều các đề tài quan trọng khác: algorithmic number theory, algorithmic coding theory, computational biology, v.v.

Chú ý: Ngoài ra, không thể nghiên cứu thuật toán hiện đại mà không có hiểu biết sâu sắc về lý thuyết độ phức tạp (computational complexity theory), lý thuyết đồ thị và toán rời rạc, lý thuyết xác suất và lý thuyết thông tin, toán tối ưu và toán ứng dụng, thậm chí cả hình học và giải tích cơ bản (cần cho computational geometry), hay lý thuyết số (cần cho các thuật toán cryptography). Tôi sẽ giới thiệu vài quyển về các đề tài này trong vài ngày tới.

## 3. Combinatorics (bao gồm lý thuyết đồ thị và toán rời rạc).

Combinatorics rất rộng, liên quan mật thiết đến rất nhiều nhánh khác nhau của toán học và khoa học máy tính. Dưới đây tôi chỉ liệt kê một sanh sách các sách tôi đã đọc và thấy hữu dụng trong nghiên cứu và trong phát triển tư duy toán học cho KHMT. Nghĩa là không kể những thứ hữu dụng mà tôi không biết gì cả như Additive Combinatorics của bác Terry Tao và bác Vũ Hà Văn.

### 3.1 Toán rời rạc phổ thông.

Hiển nhiên sinh viên học KHMT phải biết toán rời rạc. Tuy nhiên, tôi cực kỳ khó chịu với loại toán rời rạc thường được dạy ở bậc đại học nói chung, vì hai lý do: (1) lớp toán rời rạc kiểu này không chuẩn bị đủ kiến thức cho sinh viên học thêm lên, (2) và nó cho sinh viên một bức tranh bèm nhèm về toán rời rạc, dễ làm sinh viên hiểu không đúng về tầm mức của toán rời rạc. Dĩ nhiên tôi hiểu rằng chương trình đại học thì có giới hạn, còn bể kiến thức thì vô cùng, do đó cái “khó chịu” này của tôi không có cơ sở, Chỉ nhân đây càm ràm để “xả stress” là chính.

Có bốn quyển sách “phải đọc” về toán rời rạc cho sinh viên học KHMT (và cả sinh viên toán):

- J. H. van Lint and R. M. Wilson, A Course in Combinatorics, Cambridge University Press; 2nd edition (December 15, 2001). Rất tuyệt vời! Mỗi chương là một đề tài riêng biệt, từ đồ thị đến generating functions, từ design theory đến coding theory, từ q-series đến extremal set theory, v.v. đều có cả. Đa số các bài tập đều không tầm thường. Nếu bạn muốn biết combinatorics thật sự là gì, mà không có thời gian đọc nhiều quá, thì quyển này là bắt buộc!
- Ronald L. Graham, Donald E. Knuth, Oren Patashnik, Concrete Mathematics: A Foundation for Computer Science, Addison-Wesley Professional. Viết bởi computer scientists cho computer scientists. Tất cả những thứ sinh viên KHMT cần biết về asymptotic analysis. Kiểu Knuth. Nghĩa là cực kỳ cụ thể và chi tiết về phương pháp. Dĩ nhiên, phạm vi của quyển này rất hẹp, vì đề tài và đối tượng rất cụ thể.
- Laszlo Lovasz, Combinatorial Problems and Exercises, American Mathematical Society; 2 edition (June 26, 2007). Vừa ra 2nd edition. Cách duy nhất để học toán rời rạc là làm thật nhiều bài tập. Bạn hoàn toàn có thể trở thành một chuyên gia hạng ruồi về graph theory và extremal set theory bằng cách ngồi giải bài tập trong sách này. Nếu bạn đang lấy lớp combinatorics nào đó, nhiều khả năng là thầy của bạn lấy một vài bài tập trong này ra làm bài tập về nhà hoặc cả bài kiểm tra.
- Martin Aigner, Günter M. Ziegler, and K.H. Hofmann, Proofs from THE BOOK, Springer; 3rd ed. edition (November 13, 2003). Tôi không biết là quyển này đã ra đến 3rd edition, tôi chỉ có 1st edition. Nói đúng ra, quyển này không phải viết về toán rời rạc. Nhưng tư tưởng của nó lại rất tương đồng với tư tưởng của toán rời rạc mà tôi cảm nhận. Khi thấy một chứng minh đẹp như mơ, Erdos hay nói rằng “chứng minh này chắc là phải nằm trong một quyển sách của thượng đế, quyển sách chứa các chứng minh đẹp nhất”. Đó là tư tưởng chính của quyển sách. Nó chứa một bộ sưu tập các chứng minh đẹp như mơ. Dân yêu toán, ai lại không mơ?

### 3.2 Lý thuyết đồ thị (bao gồm cả algebraic graph theory).

Không có nhánh nào của KHMT mà lại không cần kiến thức cơ bản về lý thuyết đồ thị. Sách mở đầu của lý thuyết đồ thị thì có cực kỳ nhiều. Tôi vẫn thường giới thiệu quyển của West cho sinh viên vì thấy nó vừa phải và phù hợp với dân máy tính. Quyển bài tập của Lovasz ở trên có vài chương về lý thuyết đồ thị rất hay. Tôi quan tâm đến algebraic graph theory nó là công cụ chính để phân tích các expander graphs (dùng cực kỳ nhiều trong complexity theory, algorithm design, randomized algorithms, coding theory, networking, v.v.)

- Douglas West, Introduction to Graph Theory, Prentice Hall; 3 edition (December 1, 2007). Tôi thấy phạm vi đề tài của quyển này rất thích hợp cho dân học KHMT, lại rõ ràng dễ hiểu. Sau khi đọc xong một quyển giới thiệu ngành như quyển này, các quyển kế tiếp đều phải đọc theo đề tài, như algebraic graph theory, extremal graph theory, graph coloring, matching theory, v.v.
- Tommy R. Jensen and Bjarne Toft, Graph Coloring Problems, Wiley-Interscience; 1st edition (December 1994). Đây là tham khảo kinh điển về các bài toán tô màu đồ thị, dùng cực nhiều trong KHMT.
- L. Lovász and M.D. Plummer, Matching Theory, Annals of Discrete Mathematics, 29, North-Holland Mathematics Studies, 121. Tôi tin rằng dân làm về graph theory và combinatorial optimization đều … bí mật đọc quyển này 🙂 Một đề tài rất đẹp và rất khó tìm thấy ở sách khác là về các Pfaffian và Permanent. Đặc biệt là về matching trên bipartite graphs thì tất cả những thứ tôi biết đều học từ quyển này ra, và đã dùng kiến thức học được trong ít nhất 5 bài báo!
- Norman Biggs, Algebraic Graph Theory, Cambridge University Press. Quyển sách be bé này giới thiệu algebraic graph theory rất tốt. Đủ để dùng làm nhiều thứ, bao gồm hiểu các thứ liên quan đến expanders.
- Dragos M. Cvetkovic, Michael Doob, Horst Sachs, Spectra of Graphs: Theory and Applications, Academic Press; 3rd Revised edition (August 1, 1997). Đây là sách tham khảo chính về algebraic graph theory.
- Fan Chung, Spectral Graph Theory, American Mathematical Society (May 1997). Sách viết rất tốt và rõ ràng. Cái dở duy nhất là bà Fan Chung lại chọn bộ Lapacian eigenvalues thay vì bộ eigenvalues của đồ thị như trong các applications thường dùng. Chuyển qua chuyển lại các kết quả rất mất thời gian.

### 3.3 Phương pháp xác suất (bao gồm random graphs).

Phương pháp xác suất là một trong những công cụ chính của theoretical computer science, với ứng dụng ở khắp mọi nơi. Trong complexity theory & algorithms ta dùng phương pháp xác suất phân tích và thiết kế PCP, randomized (approximation) algorithms, derandomization, pseudo-random number generation, v.v. Trong mạng máy tính ta có randomized routing, randomized MAC protocols, blocking analysis of switches and routers, v.v. Trong cơ sở dữ liệu gần đây phát triển mạnh probabilistic databases, v.v.

Tôi sẽ giới thiệu sách về xác suất và thống kê trong một đề mục riêng. Phần dưới đây chỉ nói riêng về phương pháp xác suất theo nghĩa của Erdos.

- Noga Alon and Joel H. Spencer, The Probabilistic Method, Wiley-Interscience; 2 Sub edition (August 24, 2000). Kinh điển! Không có gì phải bàn.
- Béla Bollobás, Random Graphs, Cambridge University Press. Lại một quyển kinh điển nữa!
- Quyển của Mitzenmacher và Upfal đã giới thiệu trong phần giải thuật.

### 3.4. Enumerative combinatorics.

- Richard Stanley, Enumerative Combinantorics Vol. 1 & 2, Cambridge University Press. Kinh điển! Chứa hầu hết tất cả những thứ mà dân khoa học máy tính cần biết về enumerative combinatorics.
- Dennis Stanton and Dennis White, Constructive combinatorics, Springer; 1 edition (May 15, 1986). Quyển này có lẽ ít người biết nhưng tôi thấy rất hay cho dân học máy tính. Nó viết về enumerative combinatorics từ góc nhìn thuật toán và bijective proofs. Tôi đã lấy lớp của cả hai vị Dennis. Bác Stanton là người thầy có ảnh hưởng lớn nhất đến triết lý giáo dục của tôi.
- David M. Bressoud, Proofs and Confirmations: The Story of the Alternating-Sign Matrix Conjecture, Cambridge University Press (August 13, 1999). Quyển này phải nói là trên cả tuyệt vời. Quyển sách nói về một conjecture rất nổi tiếng gọi là Alternating Sign Martrix Conjecture và duyệt lại toàn bộ quá trình người ta “tấn công” conjecture này. Tôi đã từng bỏ 6 tháng vật lộn với nó 🙁 . Kết thúc bằng các công trình của Zeilberger và Kuperberg. Nó tuyệt vời ở chỗ, ngoài việc dùng làm sách giáo khoa cho một vài lớp enumerative combinatorics rất tốt, nó vẽ ra rất rõ ràng quá trình phát triển và phương pháp tư duy của một nhánh toán học dựa trên một câu chuyện cụ thể, một đề tài nghiên cứu cụ thể. Terry Tao có viết một bài hàm chứa ý tưởng tương tự về tính liên thông của các phát triển trong toán. Đến bây giờ mở sách này ra đọc tôi vẫn tìm thấy những cái mới, và cả các bài toán chưa giải được. Enumerative combinatorics là “tình yêu thời niên thiếu” của tôi, và quyển này là quyển tốt nhất giải thích tại sao tôi vẫn còn … day dứt 🙂 (Trong quyển này có nói về một thuật toán tính định thức của tác giả truyện Alice lạc vào xứ thần tiên!)
- George E. Andrews, The Theory of Partitions, Cambridge University Press (July 28, 1998). George Andrews là người tìm ra những quyển sổ tay mất tích của Ramanujan. Quyển sách của ông nằm giữa giải tích, lý thuyết số, và enumerative combinatorics. Có lẽ định lý hay nhất trong sách là công thức tính tổng số integer partitions của một số nguyên bất kỳ. Đọc sách này ta sẽ thấy generating functions mạnh như thế nào, và được dùng như thế nào trong các vấn đề cực kỳ hóc búa của lý thuyết số. Ngoài ra, nó cũng là quyển sách rất tốt về các hyper-geometric series và q-series. Tuyệt cú mèo! Có một lần tôi nghe George Andrews trình bày ở một hội nghị, ông mang theo một cuộn giấy to oành in một chương trình ông viết từ hồi đầu thập niên 70 để tìm các conjectures trong enumerative combinatorics. Ông kéo cuộn giấy đi từ đầu đến cuối phòng, chưa hết một nửa.

### 3.5 Algebraic combinatorics.

Tư tưởng của nhánh này rất gần, theo một nghĩa nhất định, với các phương pháp đại số dùng trong coding theory và complexity theory hiện đại. Nó lại liên quan mật thiết đến giải tích của các hàm vuông góc. Tôi làm M.S. Thesis Toán trong nhánh này. Mặc dù bây giờ không làm về nó nữa, nhắc lại vẫn còn thấy “nhiệt huyết” bừng bừng 🙂 . Ngoài ra, nhánh này cũng là anh em cột chèo với algebraic graph theory, rất cần thiết trong cả complexity theory lẫn một số bài toán trong mạng máy tính! Đó là chưa kể liên minh sống còn với representation theory cũng lại được dùng trong KHMT (như trong loạt bài về nhân ma trận tôi đang viết dở).

- Chris Godsil, Algebraic Combinatorics, Chapman & Hall/CRC (April 1, 1993).
- Chihara, An Introduction to Orthogonal Polynomials, Routledge; 1 edition (January 1, 1978). Quyển kinh điển về các đa thức vuông góc.
- George E. Andrews, Richard Askey, Ranjan Roy, Special Functions, Cambridge University Press; New Ed edition (February 15, 2001). Tất cả những thứ bạn cần biết về các hàm đặc biệt!
- William Fulton, Young Tableaux: With Applications to Representation Theory and Geometry, Cambridge University Press (December 28, 1996).
- I. G. Macdonald, Symmetric Functions and Hall Polynomials, Oxford University Press, USA; 2 edition (June 30, 1999). Quyển này và quyển của Fulton là kinh điển về symmetric functions.

### 3.6 Extremal set theory, extremal set systems, và design theory.

Những thứ này thì dùng làm gì trong KHMT? Một vài ví dụ nhỏ: chúng liên quan mật thiết với lý thuyết thử nhóm (group testing) được dùng trong DNA library screening (bio-computing), trong thiết kế MAC protocols và thử lỗi của mạng quang (networking), và thiết kế thuật toán nói chung. Design theory lại cũng liên quan chặt chẽ với coding theory (sẽ giới thiệu sách sau) dùng trong communications và trong complexity theory.

- Konrad Engel, Sperner Theory, Cambridge University Press. Phát triển lý thuyết của một định lý rất đơn giản và hùng mạnh trong topology: định lý Sperner.
- Bela Bollobas, Combinatorics, Cambridge University Press. Nhỏ và hiệu quả!
- A. E. Brouwer, A. M. Cohen, A. Neumaier, Distance Regular Graphs, Springer (August 1989). Nhiều bài toán thiết kế các cấu trúc extremal có thể được mô hình hóa bằng distance regular graphs: một loại đồ thị rất giàu có về cấu trúc đại số, nhờ đó bài toán trở nên tổng quát hơn (dùng công cụ của đại số), và đôi khi dễ dàng hơn.
- Ding-Zhu Du and Frank K. Hwang, Combinatorial Group Testing and Its Applications, World Scientific Publishing Company; 2nd edition (May 2000). Quyển này là tham khảo chính (và duy nhất) cho lý thuyết thử nhóm. Nó là dạng monograph chứ không phải textbook, dùng làm tham khảo.

## 4. Xử lý ngôn ngữ tự nhiên (danh sách của anh Bạch Hưng Nguyên).

Sách cơ bản:

- [1] Manning & Schutze, Foundation of Statistical NLP – (có online nếu có access vào MIT library)
- [2] Jurasky & Martin, Speech&Language Procesing: An Introduction to Natural Language Processing, Computational Linguistics, and Speech Recognition, 2nd edition.

Tham khảo thêm:

- [3] James Allen, Natural Language Understanding
- [4] Fred Jelinek, Statistical Method for Speech Recognition
- [5] Xudong Huang et al, Spoken Language Processing

Lộ trình tự đọc & học trong 1 hoặc 2 học kì theo thứ tự sau

```
——–
Chương 1+2+3+4 – [1]: Introduction / Mathematical Foundations/ Linguistic Essential / Corpus-based Work
Chương 7 – [2]: Phonetics
——–
Chương 6 – [1]: Statistical Inference: n-gram Models over Sparse Data
Chương 4 – [2]: N-grams
——–
Chương 8 – [5]: Hidden Markov Models
Chương 2 – [4]: Hidden Markov Models
Chương 4 – [2]: Word Classes and Part-of-Speech Tagging
Chương 6 – [2]: Hidden Markov and Maximum Entropy Models
——–
Chương 3 – [3]: Grammar and Parsing
Chương 12 – [2]: Formal Grammars of English
Chương 11 – [1]: Probabilistic Context Free Grammar
Chương 12 – [1]: Probabilistic Parsing
Chương 13 – [2]: Parsing with Context-Free Grammars
Chương 14 – [2]: Statistical Parsing
——–
Chương 3 – [2]: Words and Transducers
——–
Chương 22 – [2]: Information Extraction
——–
Chương 25 – [2]: Machine Translation
——–
Chương 15 – [1]: Topics in Information Retrieval
——–
Chương 16 – [1]: Text Categorization
——–
```

Lộ trình này giới thiệu chuyên sâu về phương pháp thống kê NLP, mô hình n-gram , mô hình Markov ẩn, & kĩ thuật phân tích câu (parsing). Sau đó là giới thiệu sơ qua một số topics mà NLP đóng vai trò quan trọng như Trích chọn Thông Tin (Information Extraction), Dịch tự động (Machine Translation), Khai Thác Thông Tin (Information Retrieval), & Phân Loại Văn Bản (Text Categorization). Về cơ bản sau khi xong lộ trình này là đủ để bắt tay vào chuyên sâu các vấn đề trong NLP. Rất nhiều topics của NLP không đề cập trong lộ trình này ví dụ như: Các máy Hữu hạn trạng thái (Finite-state Machines), Các kĩ thuật học máy (Machine Learning techniques), Nhận dạng tiếng nói (Speech Recognition), Tổng hợp tiếng nói (Speech Synthesis), Hệ thống Hỏi-Đáp (Q&A systems).

Sẽ tiếp tục cập nhật! Không biết bao giờ mới xong.