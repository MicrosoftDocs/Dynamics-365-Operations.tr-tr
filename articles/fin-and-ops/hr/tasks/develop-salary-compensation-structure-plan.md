--- 
title: "Maaş/ücret yapısı ve planları geliştirme"
description: "Bu görev kılavuzu, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda açıklamalar içerir."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63a02a64ff28531bae950f1b61d9167eaa0b0373
ms.openlocfilehash: 7fd32467cfbc8c30b398659d16b268f183b6b3d3
ms.contentlocale: tr-tr
ms.lasthandoff: 11/01/2017

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Maaş/ücret yapısı ve planları geliştirme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda açıklamalar içerir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir ve bu görev Ücret ve Kazanç Yöneticilerine yöneliktir.


## <a name="create-fixed-compensation-plan"></a>Sabit ücret planı oluştur
1. Ücret yönetimi'ne tıklayın.
2. Sabit ücret planları'nı tıklayın.
3. Yeni'ye tıklayın.
4. Plan alanına bir değer yazın.
5. Açıklama alanına bir değer girin.
6. Yürürlük tarihi alanına bir tarih girin.
7. Tür alanında, Sabit ücret planının bir Bant, Derece veya Adım planı olup olmadığını seçin.
8. İzin verilen öneri onay kutusu, İşlem olayı sırasında bu plana eklenen tüm eylemler için varsayılan değer olarak işlev görür.  Önerilere izin vermek, ücreti işlerken hesaplanan kılavuz tutarı geçersiz kılmanızı sağlar.
9. Aralık dışında toleransı, belirli bir düzey için belirtilen ücret yapısı aralığının dışında kalan ücret tutarlarının nasıl ele alınacağını belirtmenize olanak tanır.  Hiçbiri değerindeki bir aralık dışında toleransı, herhangi bir ücret tutarını kullanmanızı sağlar.  Yumuşak tolerans, ücret tutarı bu düzeye ilişkin minimum referans noktası tutarından düşük olduğunda veya bu düzeye ilişkin maksimum tutardan yüksek olduğunda kullanıcıyı uyarır. Kullanıcı uyarıyı yok sayıp devam edebilir.  Sert tolerans, bir çalışanın ücreti düzeye ilişkin minimum ve maksimum referans noktalarının dışında olacak şekilde ayarlandığında hata verir ve çalışanın ücretini bu aralıkta olacak şekilde otomatik olarak düzenler.
10. İşe alma kuralı alanı, çalışanın ücretini hesaplamak için bir ücret İşleme olayı çalıştırıldığında kullanılır.  İşe alma kuralı Yüzdesi, çalışanın istihdam edildiği süreye eşit oranda dağıtılan artışı hesaplar.
11. Para birimi alanına bir değer yazın.
12. Ödeme oranı dönüştürme alanına bir değer girin veya buradan bir değer seçin.
13. Aralık kullanım matrisi bölümünü genişletin.
    * İsteğe bağlı olarak, çalışanların orta noktadaki ödemeye daha hızlı ulaşmalarını ve kendi ücret aralıklarındaki maksimum kademeye daha yavaş ulaşmalarını sağlamak için ücret kademesi kullanım kayıtları ekleyin.  
14. Bu noktada, Ücreti ayarla düğmesinin etkinleşmesi için Sabit ücret planını kaydetmeniz ve plan için ücret yapınızı tanımlamaya devam etmeniz gerekir.  Kaydet'e tıklayın.
15. Ücret ayarla'ya tıklayın.
    * Ücret yapısını oluşturmak için üç yol bulunur. 1: Bir referans noktası kümesi seçip kendi yapınızı oluşturmak için düzeyler ekleyerek tamamen yeni bir yapı oluşturun. 2: Başlangıç noktası olarak mevcut bir plandan ücret yapısını kopyalayın ve bunu yeni plan için değiştirin. 3: Mevcut bir ücret kılavuzu seçin. Ücret kılavuzu başka bir plan tarafından kullanılıyorsa, kılavuzda yapılan değişiklikler diğer plana da yansır.  
16. Mevcut ücret matrisinden yeni oluştur seçimini yapın.
17. Izgaradan kopyala alanına bir değer girin veya buradan bir değer seçin.
    * İsteğe bağlı olarak, seçilen kılavuzun kopyası olarak oluşturulacak yeni ücret kılavuzunun adını değiştirebilirsiniz.  
18. Tamam'a tıklayın.
19. Toplu değişiklik seçeneğine tıklayın.
    * Toplu değiştirme, bir veya daha fazla düzeye ve/veya referans noktasına bir yüzde veya sabit tutar artışı uygulayarak ücret matrisi tutarlarını korumanıza olanak tanır.  
20. Ayarlama tutarı alanına bir sayı girin.
21. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.
22. Kılavuza uygula'ya tıklayın.
23. Sayfayı kapatın.
    * Ücret yapısı oluşturulduktan veya seçildikten sonra, Sabit ücret planı için hangi referans noktalarının Denetim noktası olarak kullanılacağını seçebilirsiniz.  Denetim noktası, bir çalışanın Karşılaştırma Oranı hesaplamak için kullanılır.  
24. Kontrol noktası alanına bir değer girin veya buradan bir değer seçin.
25. Sayfayı kapatın.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Yeni Sabit ücret planı için uygunluk kuralı oluştur
    * Yeni sabit ücret planı, plan için Uygunluk kuralları tanımlanana kadar bir çalışana atanamaz.  
1. Uygunluk kuralları'na tıklayın.
2. Yeni'ye tıklayın.
3. Uygunluk alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Yürürlük tarihi alanına bir tarih girin.
    * Uygunluk kuralları hem Sabit hem de Değişken ücret planları için kullanılır.  Tür alanında, bu uygunluk kuralları kümesinin hangi plan türü için olduğunu seçin.  
6. Plan alanında bir değer girin veya bir değer seçin.
    * Bir çalışanın ücret planına uygun olması için karşılaması gereken ölçütü seçin. Ölçüt şunlar olabilir: Departman, İşçi sendikası, Konum (Ücret bölgesi), İş, Görev, İş türü veya Ücret düzeyi. Bir çalışanın ücret planına uygun olması için belirtilen tüm ölçütleri karşılaması gerekir. Herhangi bir ölçüt seçilmezse, tüm çalışanlar ücret planı için uygun olur. Bir çalışanın uygunluk kuralında belirtilen ölçüte uymuyorsa veya ücret planı için uygunluk kuralı belirtilmediyse, ücret planı bir çalışan için Sabit ücret kaydı oluşturma sırasında arama yapıldığında görüntülenmez.  
7. Sayfayı kapatın.
8. Sayfayı kapatın.


