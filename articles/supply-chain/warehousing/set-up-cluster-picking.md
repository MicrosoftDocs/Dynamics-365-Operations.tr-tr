---
title: Küme malzeme çekme ayarlama
description: Bu konu küme malzeme çekmenin nasıl ayarlanacağını ve küme malzeme çekmeyle madde onayının nasıl uygulanacağını açıklar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da11a474e1bb031fac26e04c91cbdbab5f62eb0b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977365"
---
# <a name="set-up-cluster-picking"></a>Küme malzeme çekme ayarlama

[!include[banner](../includes/banner.md)]

Bu konu çalışanlara aynı anda birden çok iş emri için tek bir yerleşimden maddeleri çekebilmeleri için mobil cihazlardan malzeme çekme işlerini kümeler halinde gruplandırma olanağı sağlamayı açıklar. Buna *küme malzeme çekme* denir.

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

1. Mobil cihaz menü öğesinden iş onayı için kurulum formunu açın: **Ambar yönetimi** \> **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**.

1. Mobil cihaz menü öğesinden **İş onayı ayarını** açın. **Ürün onayı** seçeneği tarandığında her stok parçasını mobil cihazınızdan doğrulamanıza olanak tanır.
