---
title: Bakım talepleri oluştur
description: Bu konuda Kıymet Yönetimi'nde bakım talepleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a85125853b3b69d33f07249e0d2aa7592de1cc8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253434"
---
# <a name="create-maintenance-requests"></a>Bakım talepleri oluştur

[!include [banner](../../includes/banner.md)]

 

Bakım görevlileri veya üretim çalışanları, ekipmanların onarımını gerektiğini keşfeder ancak onarım işi hemen yapılamazsa bakım talepleri kullanılabilir.

**Örnek:** Bir bakım görevlisi bir onarım yaparken, aynı bölgedeki başka bir varlığa hizmet verilmesi gerektiğini keşfeder. Ancak, bakım görevlisinin onarım işini yapmak için zamanı veya gerekli yedek parçaları yoktur. Bu nedenle, o varlık üzerinde bir bakım talebi oluşturur ve sorunun kısa bir açıklamasını girer.

**Tüm varlıklar** ya da **Etkin varlıklar** sayfasının sağ tarafındaki **İlgili bilgiler** panelinin **Etkin bakım talepleri** bölümünde (**Varlık yönetimi** \> **Ortak** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**) seçili varlığa iliştirilmiş etkin bakım taleplerinin gösterir.

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.
2. **Yeni**'yi seçin.
3. **İstek oluştur** iletişim kutusunda **Bakım talebi türü** alanında bakım talebi türünü seçin. Varsayılan tür önerilir.
4. **Açıklama** alanına, bakım talebini kısaca açıklayan bir ad veya başlık girin.
5. **İşlem yapılacak yerleşim** ve **Varlık** alanlarında, gerektiği gibi işlem yapılacak yerleşim ya da bir varlık veya işlem yapılacak yerleşim ve bir varlığın birleşimini seçin. Bir varlık seçmeden bir bakım talebi oluşturabilir ve varlık, bakım talebine daha sonra eklenebilir. Oturum açan bir bakım görevlisi bir varlıkla ilgili bir kaynakla ilişkiliyse **Varlık** alanı otomatik olarak ayarlanır.

    Bir bakım talebi zaten seçili varlığa bağlıysa varolan bakım isteğinin kimliği hakkında sizi bilgilerindirmek için **İstek oluştur** iletişim kutusunun üst kısmında bir ileti çubuğu görüntülenir. Bir mesaj çubuğu, varlık bir garanti sözleşmesi ile kapsamında ise size bildirir.

6. **Hizmet düzeyi** alanında, isteğin aciliyetini belirten bir hizmet düzeyi seçin.
7. 5. adımda bir valık seçtiyseniz **Hata belirtisi**, **Hata alanı** ve **Hata türü** alanılarını kullanarak bir arıza kaydı oluşturabilirsiniz.
8. Bakım taleb, bakım kesintisi süresine neden olursa kesinti süresinin başlangıç tarihi ve saatini girin.

    **Başlatan** alanı otomatik olarak adınıza ayarlanır.

10. **Fiili başlangıç** alanı otomatik olarak mevcut tarih ve saat olarak ayarlanır. Ancak, değerleri istediğiniz gibi değiştirebilirsiniz.
11. **Notlar** alanında, gerekli olan ek notları girin.
12. **Tamam**'ı seçin.

![Bakım talebi oluştur](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Bakım taleplerinin sonraki işlemesi

Bir bakım talebi oluşturulduktan sonra ancak bir iş emrine dönüştürülmeden önce üzerinde çeşitli bilgiler güncelleştirilmelidir. Genellikle, bir planlayıcı veya başka bir yönetici personel bu görevi tamamlar.

- **Tüm bakım talepleri** veya **Etkin bakım talepleri** sayfasında çalışılacak isteği seçin ve **Düzenle**'yi seçin.

Ayrıntılar görünümünde, çeşitli bilgileri güncelleştirebilirsiniz. Burada bazı örnekler verilmiştir:

- Varlığı seçin ve doğrulayın. Daha sonra farklı bir varlık seçmeniz gerekiyorsa **Varlık doğrulandı** seçeneğini **Hayır** olarak ayarlayabilirsiniz.
- Sorumlu bir bakım görevlisi grubu ve/veya sorumlu bir bakım görevlisini seçin. Gerekli kurulum hakkında daha fazla bilgi için bkz: [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).
- Bir bakım işi türü seçin ve bu bilgiler alakalı ise ilgili bakım iş çeşidi ve bir zanaat seçin.
- **Enlem** ve **Boylam** alanlarında coğrafi koordinatları girin. Bir bakım talebine eklenen koordinatlar otomatik olarak ilgili iş emri için aktarılır. 

![Bakım talebini güncelleştirme](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Bir bakım talebi oluşturduğunuzda bir varlık seçerseniz varlığa bir hata ekleyebilirsiniz. Bakım talebi oluşturulduktan sonra ihtiyacınız olursa daha fazla hata ekleyebilirsiniz. Hata eklemek için **Tüm bakım talepleri** sayfasından **Varlık hatası**'nı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]