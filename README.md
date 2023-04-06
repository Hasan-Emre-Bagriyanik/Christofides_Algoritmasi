# Christofides_Algoritmasi
<br>
## Christofides algoritması amacı ne için kullanıldığı/kullanılabileceği ve çalışma şekli aşağıdaki gibidir:
<br><br>

Christofides algoritması, Euler döngüsü bulunmayan ağırlıklı bir graf için yaklaşık bir çözüm bulmak için kullanılan bir algoritmadır. Bu algoritma, kısmen Hamilton çevresi bulunan ağırlıklı bir grafda, minimum ağırlıklı Hamilton çevresini bulmak için kullanılabilecek bir yaklaşık algoritmadır.

Algoritmanın çalışma şekli şu şekildedir:

    1- Verilen ağırlıklı grafın minimum ağırlıklı çiftler eşleştirilmesi bulunur. Bu adım, grafın en küçük ağırlıklı çiftler eşleştirilmesini bulan standart bir algoritma olan Edmonds algoritması ile yapılır.

    2- Oluşan eşleştirmeyle birlikte, grafın Euler döngüsü bulunur. Bu, eşleştirme tarafından kapsanmayan tüm düğümlerin bir çifti bulunur ve bunların arasındaki yol Euler yolu olarak eklenir.

    3- Euler yolu, Hamilton yolu olacak şekilde değiştirilir. Bu, başlangıç düğümünden başlayarak her düğümün bir kez ziyaret edildiği bir döngü oluşturmak    için gerekli düğümlerin eklenmesiyle yapılır.

    4- Hamilton yolunun ağırlığı hesaplanır ve minimum ağırlıklı Hamilton çevresi bulunur.

Christofides algoritması, birçok problemin pratik çözümleri için kullanılabilir. Örneğin, seyahat eden satıcı probleminin çözümünde kullanılabilir. Ayrıca, genetik kodlamada da kullanılır ve proteinlerin şekillerini belirlemek için kullanılan moleküler dinamik simülasyonlarında kullanılır.
<br><br><br>


## Christofides algoritması calışma zamanı analizi ve En iyi, En Kötü, Ortalama sınırları açıklamalı olarak belirtilecektir. Sadece sınır belirtilmeyecektir, nasıl bulunduğu anlatılacaktır:
<br>

Christofides algoritmasının çalışma zamanı, minimum ağırlıklı çiftler eşleştirilmesi için kullanılan Edmonds algoritmasının çalışma zamanı O(EV^2) ve Euler döngüsünün bulunması için kullanılan algoritmanın çalışma zamanı O(E+VlogV)'dir. Hamilton yolu oluşturma adımı ise en kötü durumda O(V^2)'dir. Toplam çalışma zamanı O(EV^2 + E + VlogV + V^2) olarak hesaplanabilir. Ancak, Euler döngüsü ve Hamilton yolu oluşturma adımları yaklaşık olarak yapılır, bu nedenle algoritmanın çalışma zamanı pratikte genellikle O(EVlogV)'dir.

    1-En iyi durum, grafın tamamen düzensiz olduğu ve minimum ağırlıklı Hamilton çevresinin en az bir ağırlıklı kenara sahip olduğu durumdur. Bu durumda, algoritmanın çıktısı optimumdur.

    2-En kötü durum, graf tamamen düzenli olduğunda ve minimum ağırlıklı Hamilton çevresi, en küçük ağırlıklı kenara sahip çevre ile aynı olduğunda gerçekleşir. Bu durumda, algoritmanın yaklaşık çözümü optimumdan daha kötü olabilir.

    3-Ortalama durum, çoğu durumda yaklaşık çözümün optimalden çok uzak olmayacağı durumdur. Christofides algoritması, özellikle büyük graf boyutları için etkili bir yaklaşım sağlar ve pratikte çoğu durumda yeterince iyi bir çözüm üretir.
