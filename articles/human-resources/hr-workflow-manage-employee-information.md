---
title: Personel bilgilerini yönetmek için iş akışları kullanma
description: Bu makalede, personel bilgisini yönetmek için iş akışlarını nasıl kullanabileceğiniz açıklanmaktadır.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750747"
---
# <a name="use-workflows-to-manage-employee-information"></a>Personel bilgilerini yönetmek için iş akışları kullanma

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, personel bilgisini yönetmek için İnsan kaynakları için iş akışı yeteneğini nasıl kullanabileceğinizi açıklar. Örneğin, bir iş akışını bir pozisyonla ilişkilendirebilir ve çalışanların kendi kayıtlarını değiştirdiklerinde başlatılan bir onay iş akışı yapılandırabilirsiniz.

İnsan kaynakları için iş akışı kabiliyeti, insan kaynakları faaliyetlerini yönetmek için çok sayıda iş akışı sağlar. Ek olarak, belirli iş akışlarını değiştirebilmeniz ve onları bir raporlama hiyerarşisiyle ilişkilendirebilmeniz için çok sayıda seçenek kullanabilmektedir. İş akışları, yöneticilerin personel bilgilerinin çeşitli türlerinde değişik yapmalarını kolaylaştırmak için mevcuttur. İş akışını bir pozisyon ile ilişkilendirebilirsiniz. Daha sonra, personeller kendi personel kayıtlarını değiştirirlerse, yeni bilgiler kaydedilemeden önce onay gerektiren bir iş akışı başlatılır. İş akışları, değişiklikleri daha etkin şekilde yönetebilmeniz ve personel bilgilerinizi daha doğru tutabilmeniz için aşağıdaki türde bilgiler için önceden tanımlıdır:

-   Kimlik numaraları
-   Kurslar
-   Eğitim
-   Resim
-   Ödünç verilen maddeler
-   Mesleki deneyim
-   Proje deneyimi
-   Yetenekler
-   Güven gerektiren pozisyonlar
-   İnsan kaynakları eylemleri
-   Kurs kaydı

Personeller işe alındıklarını, transfer edildiklerinde veya işten çıkarıldıklarında, iş akışı bir gözden geçirme işlemi içerebilir. Bu şekilde, bir belge gözden geçirilebilir veya bir eylemin koşulları, iş akışının bir parçası tanımlanabilir. Gözden geçirme işlemi tamamlandığında, belge veya eylem tamamlanır ve iş akışını son onayı adımına taşınır.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>İş akışını bir pozisyon hiyerarşisiyle ilişkilendirin.

Bir iş akışını, yapılandırdığınız herhangi bir pozisyon hiyerarşisiyle ilişkilendirebilirsiniz. İş akışı yönlendirmesi için iki hiyerarşi türü kullanılır: **Yönetim** ve **Yapılandırılabilir**.

- **Yönetim** hiyerarşisi, şirketin veya kuruluşun raporlama yapısını temsil eder. Bu hiyerarşi türü hakkında daha fazla bilgi için bkz. [Rapor verilen pozisyon](hr-personnel-positions.md#reports-to-position).
- **Yapılandırılabilir** hiyerarşi, bir matrisi veya özel hiyerarşiyi temsil eder. Bu hiyerarşi türü hakkında daha fazla bilgi için bkz. [İlişkiler](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Yönetim hiyerarşisi örneği

Bir çalışan yeni bir bilgisayar için satın alma isteği gönderdiğinde isteğin çalışanın yöneticisine ve atlama düzeyi yöneticisine yönlendirildiği bir iş akışı yapılandırabilirsiniz. İş akışı adımını yapılandırırken **Atama türü** alanını **Hiyerarşi** olarak ayarlayın. Ardından **Hiyerarşi türü** sekmesi kullanılabilir hale gelir. Bu örnekte, **Yönetim** hiyerarşisini seçin.

### <a name="configurable-hierarchy-example"></a>Yapılandırılabilir hiyerarşi örneği

Bir pozisyon, bir matris raporlama hiyerarşisi ile ilişkili ise, belirli bir projenin giderlerinin bir çalışanın yöneticisi yerine proje liderine yönlendirildiği bir iş akışı yapılandırabilirsiniz. Bu durumda, **Atama türü** alanını **Hiyerarşi** olarak ayarlayın. Ardından **Hiyerarşi türü** sekmesinde **Yapılandırılabilir** hiyerarşiyi seçin. İş akışı ayarlandıktan sonra iş akışı yönlendirmesi için kullanılması gereken hiyerarşiyi seçmek için **İş akışı kurulumu** sayfasında hiyerarşiyi **ilişkilendir**'i seçin.

> [!IMPORTANT]
> İş akışı onayı için bir belge, işlem veya ana kayıt gönderildiğinde belgenin sonraki aşamada kime yönlendirileceğini belirlemek için gönderenin birincil pozisyonu kullanılır.

### <a name="hierarchy-setting-in-workflow-parameters"></a>İş akışı parametrelerinde hiyerarşi ayarı

1. **İş akışı parametreleri** sayfasında, **Hiyerarşi yönlendirme**'yi seçin.
2. Varsayılan olarak, **Pozisyon hiyerarşisi kullan** seçeneği **Hayır** olarak ayarlanır. Bu durumda, iş akışı hiyerarşiye yönlendirildiğinde çalışanın birincil pozisyonu kullanılır. İş akış hiyerarşiye yönlendirildiğinde pozisyon üst öğesinin kullanılmasını sağlamak için bu seçeneği **Evet** olarak ayarlayın.

### <a name="additional-example"></a>Ek örnek 

Grace Sturman adlı çalışanın iki pozisyonu vardır: danışman ve eğitimci. Grace'in birincil pozisyonu eğitimcidir. Yeni çalışanları eğitmediğinde danışmanlık işi yapmaktadır. Grace, birincil pozisyonu için insan kaynakları müdürü Claire'e rapor vermektedir. Claire, Charlie'ye rapor vermektedir. Grace, projeye bağlı olarak danışmanlık pozisyonu için birden çok noktalı çizgi ilişkisine sahiptir.

Grace'in şirketi, **Yapılandırılabilir** hiyerarşiyi (matris/proje tabanlı hiyerarşiler) temel alan iş akışı yönlendirme kuralları oluşturmaktadır. Bu hiyerarşide Grace'in danışmanlık pozisyonu kullanılmaktadır. Belge onay için Grace'e yönlendirilirken **Pozisyon hiyerarşisini kullan** seçeneği **Hayır** olarak ayarlanırsa iş akışı belgenin sonraki aşamada nereye yönlendirileceğini belirlemek için birincil pozisyonuna (eğitmenlik) bakar. Bu durumda, belge önce Claire'e, ardından Charlie'ye yönlendirilir. Bu seçenek **Evet** olarak ayarlanırsa ve iş akışında **Yapılandırılabilir** hiyerarşi kullanılıyorsa iş akışı, belgenin sonraki aşamada nereye yönlendirileceğini belirlemek için Grace'in danışmanlık pozisyonuna ve raporlama ilişkisine bakar.

### <a name="configure-a-human-resources-workflow"></a>İnsan kaynakları iş akışı yapılandırma
Çalışanlar kişisel kimlik saptamalarında değişiklik talep ettiklerinde başlatılacak basit bir iş akışı yapılandırmak için şu adımları izleyin.

1.  **İnsan Kaynakları iş akışları** sayfasında **Yeni**'yi seçin.
2.  Kullanılabilir iş akışları listesinden **Kimlik saptama numaraları**'nı seçin.
3.  İş akışı tasarımcısını açmak için **Çalıştır**'ı seçin ve ardından kullanıcı adınızı ve parolanızı girin.
4.  İş akışı öğeleri listesinden **Kimlik saptama numarasını** öğesini, tasarımcı tuvaline taşıyın.
5.  Onay öğesini **Başlat** ve **Bitir** ile bağlayın.
6.  **Öğeyi onaylamak** için çift dokunun (veya çift tıklatın), seçin ve tutun (veya sağ tıklatın) ve sonra da **Özellikler**'i seçin.
7.  İş öğesi yönergeleri eklemek için şu adımları izleyin:

    1.  **Atama**'yı seçin ve sonra atama türü altında **Hiyerarşi**'yi seçin.
    2.  **Hiyerarşi** seçimi altında **Yapılandırılabilir hiyerarşi**'yi seçin.
    3.  Bir durdurma koşulu ekleyin ve sayfayı kapatın.

8.  Ek yönergeleri tamamlayın.
9.  **Kaydet ve kapat**'ı seçin. Yeni iş akışını etkinleştirip iletişim kutusu açılınca **Etkinleştir**'i seçin.
10. **İnsan Kaynakları** &gt; **Pozisyonlar** &gt; **Pozisyon hiyerarşi türleri**'ne gidin.
11. **Matris**'i seçin.
12. **Çalışan kimlik saptama numarası**'nı iş akışı listesine ekleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Adres değişikliklerini görüntüle ve yönet](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
