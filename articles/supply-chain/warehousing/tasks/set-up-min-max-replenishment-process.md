--- 
title: "Minimum-maksimum stok yenileme işlemini ayarlama"
description: "Bu yordam, minimum/maksimum stok yenileme stratejisini kullanan yeni bir stok yenileme işlemini nasıl ayarlayacağınızı gösterir."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Minimum-maksimum stok yenileme işlemini ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, minimum/maksimum stok yenileme stratejisini kullanan yeni bir stok yenileme işlemini nasıl ayarlayacağınızı gösterir. Stok minimum düzeyin altına düştüğünde, konumun yenilenmesi için iş oluşturulur. Bu yordam ayrıca sabit çekme konumlarının, stok belirli bir seviyenin altına düşse bile yeniden nasıl stoklanacağını ve bir toplu iş kullanarak stok yenileme işleminin düzenli aralıklarla nasıl çalıştırılacağını göstermektedir. Bu görevler genellikle ambar Yöneticisi tarafından yerine getirilir. Bu yordamı, notlardaki örnek değerleri USMF demo veri şirketini kullanarak ya da kendi verileriniz ile çalıştırabilirsiniz. Kendi verilerinizi kullanıyorsanız, Ambar yönetim işlemleri için etkin bir ambara sahip olduğunuzdan emin olun.


## <a name="create-a-fixed-picking-location"></a>Sabit bir çekme konumu oluşturun
1. Ambar yönetimi > Kurulum > Ambar > Sabit konumlar öğesine gidin.
    * Bu, min-maks stok yenileme için tercihe bağlı bir görevdir fakat sabit bir çekme konumu kullanıyorsanız, bu stoğun minimum seviyenin altın düşmesi durumunda bile yenilenmesini sağlar, çünkü sistem hangi maddelerin yenilenmesinin gerektiğini belirleyebilir, hiç kalmamış olsalar bile.  
2. Yeni'ye tıklayın.
3. Madde numarası alanında bir değer girin veya seçin.
    * USMF kullanıyorsanız, A0001 öğesini seçebilirsiniz.  
4. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * USMF kullanıyorsanız, site 2'yi seçebilirsiniz.  
5. Ambar alanında bir değer girin veya bir değer seçin.
    * USMF kullanıyorsanız, ambar 24'ü seçebilirsiniz.  
6. Konum alanına bir değer girin veya buradan bir değer seçin.
    * USMF kullanıyorsanız, CP-003'ü seçebilirsiniz.  
7. Sayfayı kapatın.

## <a name="create-a-replenishment-location-directive"></a>Bir stok yenileme konum yönergesi oluşturun
1. Ambar yönetimi > Kurulum > Konum yönergeleri öğesine gidin.
    * Konum yönergeleri stok yenileme işleminde maddelerin çekileceğini yeri belirlemek için kullanılır.  
2. İş siparişi türü alanında 'Stok Yenileme' seçin.
3. Yeni'ye tıklayın.
4. İsim alanına bir değer yazın.
5. İş türü alanında 'Malzeme çekme öğesini seçin.
6. Tesis alanına bir değer girin veya buradan bir değer seçin.
    * USMF kullanıyorsanız, site 2'yi seçebilirsiniz.  
7. Ambar alanında bir değer girin veya bir değer seçin.
    * USMF kullanıyorsanız, ambar 24'ü seçebilirsiniz.  
8. Kaydet'e tıklayın.
9. Yeni'ye tıklayın.
10. Listede, seçili satırı işaretleyin.
11. Alıcı miktarı alanına bir sayı girin.
    * Örneğin 9999 olarak ayarlayın.  
12. Bölünmüş çekmelere izin ver onay kutusunu seçin.
    * Bu seçeneği belirlerseniz, iş oluşturma süreci iş satırları miktarlarının birden fazla konuma bölünmesine izin verecektir.  
13. Kaydet'e tıklayın.
14. Yeni'ye tıklayın.
15. Listede, seçili satırı işaretleyin.
16. İsim alanına bir değer yazın.
17. Kaydet'e tıklayın.
18. Sorguyu düzenle'ye tıklayın.
    * Bu sorguyu düzenleyip, stok yenilenme işleminde stokun nereden seçilebileceğine dair kısıtlama ekleyebilirsiniz. Örneğin, stok sadece ambarın Toplu alanından kullanılabiliyor olabilir.  
19. Tamam'a tıklayın.
20. Sayfayı kapatın.

## <a name="create-a-replenishment-work-template"></a>Bir Stok yenileme iş şablonu oluşturun
1. Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.
    * İş şablonu, sistemi min/maks stok yenileme işinin nasıl oluşturulacağına dair yönlendirmek için kullanılır. En düşük gereksinim olarak,çekme ve yerine koyma için bir iş şablonu satırı olmalıdır. İş şablonu, tüm gerekli bilgiler doldurulmuş olana kadar geçersiz olduğunu söyleyecektir.  
2. İş siparişi türü alanında 'Stok Yenileme' seçin.
3. Yeni'ye tıklayın.
4. İş şablonu alanında bir değer girin.
5. Kaydet'e tıklayın.
6. Yeni'ye tıklayın.
7. İş türü alanında 'Malzeme çekme öğesini seçin.
8. İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.
    * Bunun stok yenileme ile ilgili bir iş sınıf olması gerekir. USMF kullanıyorsanız, Stok Yenileme'yi seçin.  
9. Yeni'ye tıklayın.
10. Listede, seçili satırı işaretleyin.
11. İş türü alanında, 'Yerine koyma'yı seçin.
12. İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.
13. Kaydet'e tıklayın.
14. Sayfayı kapatın.

## <a name="create-a-new-replenishment-template"></a>Yeni bir stok yenileme şablonu oluşturun
1. Ambar yönetimi > Kurulum > Stok yenileme > Stok yenileme şablonları öğesine gidin.
    * Stok yenileme şablonu, maddeleri ve miktarları ve yenilenecek konumu tanımlamak için kullanılır.  
2. Yeni'ye tıklayın.
3. Stok yenileme şablonu alanında bir değer girin.
    * Şablonun min/maks stok yenileme için olduğunu belirtecek bir ad verin.  
4. Açıklama alanına bir değer girin.
5. Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver onay kutusunu işaretleyin.
    * Bu seçeneği belirlerseniz, dalga talep stok yenilemesinin, min/maks stok yenileme ile ilgili miktarları tüketmesini talep eder. Örneğin bu, min/maks stok yenileme işi derhal işlenmeyecekse, gereksiz stok yenileme işinin talep edilmesinin oluşturulmasının önüne geçmek için kullanışlı olabilir.  
6. Yeni'ye tıklayın.
7. Sıra numarası alanına bir numara girin.
8. Açıklama alanına bir değer girin.
9. Listede, seçili satırı işaretleyin.
10. Stok yenileme birimi alanına bir değer girin veya bir değer seçin.
    * Örneğin, adet seçin. Bu seçenek zorunludur. Bu stoktaki minimum ve maksimum seviyeler için tanımlanmış birim ile kıyasla, farklı bir ölçüm birimini stok yenileme işi için belirlemenize izin verir.  
11. İş şablonu alanında bir değer girin veya bir değer seçin.
    * Daha önce oluşturduğunuz iş şablonunu seçin.  
12. Minimum miktar alanında, bir sayı girin.
    * Stok yenilemeyi tetiklemesi gereken minimum miktarı seçin. Örneğin, bu ayarlar için 50. Eğer sabit bir konumu yeniliyorsanız ve Sabit konumları yenile seçeneği Evet olarak ayarlanmış ise bu ayarı sıfır olarak bırakmak mümkündür. Performans artırmak için Sadece sabit konumları yenile seçeneğini seçmenizi öneririz.  
13. Maksimum miktar alanında, bir sayı girin.
    * Örneğin, bunu 100'e ayarlayın.  
14. Birim alanına bir değer girin veya buradan bir değer seçin.
    * Minimum ve maksimum miktarlar için birimi atayın. Örneğin bunu, adet olarak ayarlayın.  
15. Boş sabit konumları yenile onay kutusunu işaretleyin.
    * Bu onay kutusunu sabit konumları boş olduklarında yenilemek için işaretleyin. Aksi takdirde, yalnızca elde bir miktar bulunan konumlar yenilenecektir.  
16. Sadece boş sabit konumları yenile onay kutusunu işaretleyin.
17. Ürünleri seç'i tıklatın.
    * Bu, hangi ürünlerin yenilenebileceğini tanımlayabileceğiniz bir yerdir. Eğer Sabit çekme konumları seçeneği belirlendiyse, bu sorguda ayrıca konumları tanımlamanız gerekmektedir. Değişken özgü sorgular ve ayrıca ürüne özgü sorgular da kullanılabilir.  
18. Maddeler satırını seçin.
19. Ölçütler alanına bir değer yazın.
    * Sabit konumlarda yenilenmesi gereken öğeleri seçin. Örneğin, A ile başlayan tüm madde numaralarını seçmek için A* girin.  
20. Ekle öğesini tıklatın.
    * Stok yenileme işini, ambarın belirli bir bölgesindeki sabit çekme konumlarına kısıtlamak için, konum varlığını ekleyin (eğer halihazırda mevcut değilse).  
21. Listede, seçili satırı işaretleyin.
22. Tablo alanını Konumlar olarak ayarlayın.
23. Konum alanında, Konum profil kimliği'ni seçin.
24. Ölçütler alanında bir değer girin veya seçin.
25. Tamam'a tıklayın.
26. Sayfayı kapatın.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Stok yenileme işlemini toplu iş olarak çalışmak için ayarlayın
1. Ambar yönetimi > Stok yenileme > Stok yenilemeleri öğesine gidin.
    * Stok yenilemeleri sayfası, yenilemeyi bir toplu iş olarak çalıştırmak veya el ile başlatılmasını gerektirecek şekilde ayarlayabilmeniz için olanak sağlar.  
2. Filtre'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ölçütler alanında bir değer girin veya seçin.
5. Tamam'ı tıklatın.
6. Arka planda çalıştır bölümünü genişletin.
7. Toplu işleme seçeneğini evet olarak ayarlayın.
8. Yineleme'ye tıklayın.
9. Bitiş tarihi yok seçeneğini seçin.
10. Tekrar etme modelini ayarlayın.
    * Örneğin, Günler seçin.  
11. Tamam'a tıklayın.
12. Tamam'a tıklayın.


