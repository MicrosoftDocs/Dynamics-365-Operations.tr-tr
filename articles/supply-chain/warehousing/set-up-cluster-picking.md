---
title: Küme malzeme çekmeyi ayarlama
description: Bu makale küme malzeme çekmenin nasıl ayarlanacağını ve küme malzeme çekmeyle madde onayının nasıl uygulanacağını açıklar.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014777"
---
# <a name="set-up-cluster-picking"></a>Küme malzeme çekmeyi ayarlama

[!include[banner](../includes/banner.md)]

Bu makale çalışanlara aynı anda birden çok iş emri için tek bir yerleşimden maddeleri çekebilmeleri için mobil cihazlardan malzeme çekme işlerini kümeler halinde gruplandırma olanağı sağlamayı açıklar. Buna *küme malzeme çekme* denir.

## <a name="about-cluster-picking"></a>Küme malzeme çekme hakkında

İş emirleri ambara serbest bırakıldıktan sonra çalışan emirleri bir kümeye atamak için mobil cihaz kullanabilir. Küme çalışan için malzeme çekme işini düzenler. Bir iş emri bir kümeye atandığında, çalışanın iş emri için malzeme çekme işlemini gerçekleştirmek için küme malzeme çekme kullanması gerekir. Çalışan diğer malzeme çekme yöntemlerini kullanılamaz. Bir iş emri bir kümeye yanlışlıkla atanırsa, çalışanın kümeyi bozması ve yeniden oluşturması gerekir.

Gerekirse, çalışan kümeyi başka bir çalışana geçirebilir. Bu, kümenin durumunu Geçirildi olarak değiştirir. Çalışan malzeme çekme ve koyma işinin tamamlandığını belirtmek için bir mobil cihaz kullandığında, sevkiyat veya yüklemenin istemcide onaylanması gerekir.

## <a name="enable-cluster-picking"></a>Küme malzeme çekmeyi etkinleştirme

Küme malzeme çekmeyi etkinleştirmek için şunları ayarlamanız gerekir:

- **Küme profilleri** – Küme kodlarının otomatik oluşturulup oluşturulmayacağını, kullanılacak pozisyon sayısını, kümelerin ne zaman ayrılacağını ve malzeme çekme işinin nasıl sıralanıp doğrulanacağını belirtin.

- **İş şablonları** – Küme malzeme çekme için malzeme çekme içinin nasıl oluşturulacağını tanımlayın.

- **Yerleşim yönergeleri** – Maddelerin nereden çekileceğini ve nereye konulacağını belirtin.

- **Mobil cihaz menü öğeleri** – Küme malzeme çekme tarafından yönlendirilen mevcut işi kullanmak için bir mobil cihaz menüsü yapılandırın. Mobil cihazlarda görünmesi için menüyü mobil cihaz menüsüne eklemeniz gerekir.

- **Ambar Yönetimi parametreleri** – Kümeler için tanımlayıcılar oluşturmak istiyorsanız, kullanılacak numara serisini belirtin.

## <a name="set-up-a-cluster-profile"></a>Küme profili ayarlama

Küme profili ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Küme profilleri**'ne tıklayın.

1. Yeni bir profil oluşturmak için **Yeni**'ye tıklayın.

1. **Küme oluştur**'a tıklayın ve **Küme sıralama** altından **Yeni**'yi tıklayarak küme için sıralama ölçütü ayarlayın. Bu sıralama kriteri, çalışanın malzeme çekme işini hangi sırada yapacağını denetler. İhtiyaç duyduğunuz sayıda ölçüt ekleyebilirsiniz.

1. **Sıra numarası** alanında, sıralama ölçütü işlenme sırasını belirlemek için bir sayı girin.

1. **Alan adı** alanında, sıralamayı belirleyecek alanı seçin. Örneğin **WMSLocationId** alanını seçerseniz iş yerleşime göre sıralanır.

1. **Sıralama** alanında aşağıdaki seçeneklerden birini belirleyin.

| **Seçenek**     | **Açıklama**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Artan**  | Malzeme çekme işi sıralama ölçütünü temel alarak artan düzende sıralanır. Örneğin sıralama ölçütü olarak **WMSLocationId** kullanırsanız ve yerleşim kodlarının 1, 2, 3 ve 4 ise önce yerleşim 4'ten malzeme çekersiniz. |
| **Azalan** | Malzeme çekme işi sıralama ölçütünü temel alarak azalan düzende sıralanır. Örneğin sıralama ölçütü olarak **WMSLocationId** kullanırsanız ve yerleşim kodlarının 1, 2, 3 ve 4 ise önce yerleşim 1'den malzeme çekersiniz. |

## <a name="item-confirmation"></a>Madde onayı

Küme malzeme çekme uygulandığında, öğe yapılandırması maddelerin kümelere eklendiğinden emin olmak için önemlidir. Küme malzeme çekme işlemi sırasında küme malzeme çekme içerisindeki öğeleri doğrulayabilirsiniz. Kurulum ürün barkod kurulumuna dayanır.

### <a name="set-up-item-verification-with-cluster-picking"></a>Küme malzeme çekme ile madde doğrulamayı ayarlamak

1. **Ambar yönetimi** >  **Kurulum** >  **Mobil cihaz** >  **Mobil cihaz menüsü öğeleri** seçeneğine gidin.
1. Liste bölmesinde, ayarlamak istediğiniz menü öğesini seçin.
1. Eylem bölmesinde **İş onayı kurulumu**'nu seçin.
1. Aşağıdaki eylemlerden birini gerçekleştirin:
    - Ayarlamak istediğiniz **İş türü** için bir satır zaten varsa, bunu seçin ve sonra eylem bölmesinde **Düzenle** seçeneğini belirleyin.
    - Uygun bir satır yoksa, eylem bölmesinde **Yeni**'yi seçin ve sonra **İş türü**'nü uygun türe ayarlayın.
1. Yeni veya seçili satırınız için **Ürün onayı** onay kutusunu işaretleyin. Bu, çalışanların her stok parçasını mobil cihaz kullanarak doğrulamalarına olanak tanır.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]