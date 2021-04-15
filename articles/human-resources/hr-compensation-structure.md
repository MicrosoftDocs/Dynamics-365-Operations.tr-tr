---
title: Ücret yapısı geliştirme
description: Bu makale, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda sizi yönlendirir.
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75d1a05d4f94689581e2a67a13adeef6b14ac0cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800915"
---
# <a name="develop-a-compensation-structure"></a>Ücret yapısı geliştirme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makale, bir Sabit ücret planı oluşturma ve çalışanların uygunluk kuralları aracılığıyla plana kaydedilmesini sağlama konusunda sizi yönlendirir. Bu makale USMF demo verilerini kullanır ve ücret ve sosyal haklar yöneticilerine uygulanır.

## <a name="create-a-fixed-compensation-plan"></a>Sabit ücret planı oluşturma

1. **Ücret Yönetimi** seçin.

2. **Sabit ücret planları** seçin.

3. **Yeni**'yi seçin.

4. **Plan** alanına bir değer girin.

5. **Açıklama** alanında bir değer girin.

6. **Yürürlük tarihi** alanına bir tarih girin.

7. **Tür** alanında, sabit ücret planının bir **Bant**, **Derece** veya **Adım** planı olup olmadığını seçin.

8. **İzin verilen öneri onay kutusu**, İşlem olayı sırasında bu plana eklenen tüm eylemler için varsayılan değer olarak işlev görür. Önerilere izin vermek, ücreti işlerken hesaplanan kılavuz tutarı geçersiz kılmanızı sağlar.

9. **Aralık dışında toleransı**, belirli bir düzey için belirtilen ücret yapısı aralığının dışında kalan ücret tutarlarının nasıl ele alınacağını belirtmenize olanak tanır. **Aralık dışı tolerans** alanını **yok** olarak ayarlamak, herhangi bir maaş tutarını kullanmanızı sağlar. **Yumuşak tolerans**, ücret tutarı bu düzeye ilişkin minimum referans noktası tutarından düşük olduğunda veya bu düzeye ilişkin maksimum tutardan yüksek olduğunda kullanıcıyı uyarır. Kullanıcı uyarıyı yok sayıp devam edebilir. **Sert tolerans**, bir çalışanın ücreti düzeye ilişkin minimum ve maksimum referans noktalarının dışında olacak şekilde ayarlandığında hata verir ve çalışanın ücretini bu aralıkta olacak şekilde otomatik olarak düzenler.

10. **İşe alma kuralı** alanı bir çalışanın işlem olayı sırasında maaşına karşılık hesaplar. **İşe alma kuralı** **Yüzdesi**, çalışanın istihdam edildiği süreye eşit oranda dağıtılan artışı hesaplar.

11. **Para birimi** alanına bir değer yazın.

12. **Ödeme oranı dönüştürme** alanına bir değer girin veya buradan bir değer seçin.

13. **Aralık kullanım matrisi** bölümünü genişletin. İsteğe bağlı olarak, çalışanların orta noktadaki ödemeye daha hızlı ulaşmalarını ve kendi ücret aralıklarındaki maksimum kademeye daha yavaş ulaşmalarını sağlamak için ücret kademesi kullanım kayıtları ekleyin.

14. **Kaydet**'i seçin. Bu, **maaş ayarla** düğmesini etkinleştirir ve plan için maaş yapınızı tanımlamaya devam eder.

15. **Ücret ayarlama**'yı seçin. Ücret yapısı bu üç yöntemlerden birini kullanarak oluşturabilirsiniz:

    - Bir referans noktası kümesi seçip kendi yapınızı oluşturmak için düzeyler ekleyerek tamamen yeni bir yapı oluşturun.
    - Başlangıç noktası olarak mevcut bir plandan ücret yapısını kopyalayın ve bunu yeni plan için değiştirin.
    - Mevcut bir ücret kılavuzu seçin. Ücret kılavuzu başka bir plan tarafından kullanılıyorsa, kılavuzda yapılan değişiklikler diğer plana da yansır.

16. **Mevcut maaş matrisinden yeni oluştur**'u seçin.

17. **Izgaradan kopyala** alanına bir değer girin veya buradan bir değer seçin. İsteğe bağlı olarak, seçilen kılavuzun kopyası olarak oluşturulacak yeni ücret kılavuzunun adını değiştirebilirsiniz.

18. **Tamam**'ı seçin.

19. **Toplu değişiklik**'i seçin. **Toplu değiştirme**, bir veya daha fazla düzeye ve/veya referans noktasına bir yüzde veya sabit tutar artışı uygulayarak ücret matrisi tutarlarını korumanıza olanak tanır.

20. **Ayarlama tutarı** alanına bir sayı girin.

21. Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.

22. **Kılavuza uygula**'ya tıklayın.

23. Sayfayı kapatın. Ücret yapısı oluşturulduktan veya seçildikten sonra, Sabit ücret planı için hangi referans noktalarının Denetim noktası olarak kullanılacağını seçebilirsiniz. Denetim noktası, bir çalışanın Karşılaştırma Oranı hesaplamak için kullanılır.

24. **Kontrol noktası** alanına bir değer girin veya buradan bir değer seçin.

25. Sayfayı kapatın.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Sabit ücret planı için uygunluk kuralı oluştur

Yeni sabit ücret planı, plan için Uygunluk kuralları tanımlanana kadar bir çalışana atanamaz.  

1. **Uygunluk kurallarını** seçin.

2. **Yeni**'yi seçin.

3. **Uygunluk** alanına bir değer girin.

4. **Açıklama** alanında bir değer girin.

5. **Yürürlük tarihi** alanına bir tarih girin. Hem Sabit hem de Değişken ücret planları uygunluk kurallarını kullanılır. **Tür** alanında plan türünü seçin.

6. **Plan** alanına bir değer girin veya bir değer seçin. Bir çalışanın ücret planına uygun olması için karşılaması gereken ölçütü seçin. Ölçütler şunlar olabilir:

    - **Departman**
    - **Sendika**
    - **Konum** (**Ücret bölgesi**)
    - **İş**
    - **İşlev**
    - **İş türü**
    - **Tazminat düzeyi**
    
    Bir çalışanın ücret planına uygun olması için belirtilen tüm ölçütleri karşılaması gerekir. Herhangi bir ölçüt seçilmezse, tüm çalışanlar ücret planı için uygun olur. Bir çalışanın uygunluk kuralında belirtilen ölçüte uymuyorsa veya ücret planı için uygunluk kuralı belirtilmediyse, ücret planı bir çalışan için Sabit ücret kaydı oluşturma sırasında arama yapıldığında görüntülenmez.

7. Sayfayı kapatın.

8. Sayfayı kapatın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]