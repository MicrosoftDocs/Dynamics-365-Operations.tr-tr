---
title: Kalite yönetimi testleri
description: Bu makale, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle kullanılabilmesi için, testlerin nasıl oluşturulacağını açıklar.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac67ee97a4890c646daefa6b09feae25c4f15d0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857619"
---
# <a name="quality-management-tests"></a>Kalite yönetimi testleri

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle kullanılabilmesi için, testlerin nasıl oluşturulacağını açıklar.

Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için **Testler** sayfasını kullanın. Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz. Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz. Ölçüm değerleri, niceliksel testler için kullanılır. Niteleyici testler için test değişkenleri kullanılır.

- Niceliksel testler için, **Tür** alanını *Tamsayı* veya *Kesir* olarak ayarlanır. Bir ölçü birimi belirlenir. Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.
- Niteliksel testler için, **Tür** alanı *Seçenek* olarak ayarlanmıştır. Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler. Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.

İsteğe bağlı olarak test aracını bir teste de atayabilirsiniz. Ancak, test araçları, testleri kalite emirleri ile oluşturmak ve kullanmak için gerekli değildir. Daha fazla bilgi için bkz. [Kalite yönetimi test araçları](quality-test-instruments.md).

Test sonuçlarının kaydedildiği ölçü birimini belirtmek için isteğe bağlı olarak test için bir birim de belirtebilirsiniz. Örneğin, sıcaklık testine Fahrenhayt veya Santigrat derece birimini ekleyebilirsiniz.

## <a name="example-of-a-test"></a>Test örneği

Bir üretim şirketi satın alınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor. Şirket, test değişkenini (örneğin hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor. Şirket **Test grupları** sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır. Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.

## <a name="create-a-test"></a>Test oluşturun

Bir test oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Testler** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Test** – Test için benzersiz bir kod ya da ad girin.
    - **Açıklama** – Testin detaylı bir açıklamasını girin.
    - **Tür** – Testin ürettiği sonuçların türünü seçin. Niceliksel testler için *Kesir* veya *Tamsayı* seçin. Niteliksel testler için, *Seçenek* seçeneğini belirleyin.
    - **Test aracı** – Test için kullanılacak [test aracını](quality-test-instruments.md) seçin.
    - **Birim** – **Tür** alanında *Kesir* veya *Tamsayı* seçtiyseniz (test bir niceliksel test ise), test sonuçlarının kaydedilmesi gereken ölçü birimini seçin.

1. Sayfayı kapatın.

> [!NOTE]
> Testi kaydettikten sonra, ızgarada **Tür** alanını düzenleyemezsiniz. Test için kaydedilecek test sonuçlarının türünü değiştirmeniz gerekiyorsa, Eylem Bölmesinde **Kalite test türünü değiştir**'i seçin. **Kalite test türünü değiştir** iletişim kutusunda, **Yeni tür** alanını istediğiniz türe ayarlayın ve sonra iletişim kutusunu kapatmak için **Tamam**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi test gereçleri](quality-test-instruments.md)
- [Kalite yönetimi test grupları](quality-test-groups.md)
- [Kalite yönetimi test değişkenleri](quality-test-variables.md)
- [Kalite ilişkileri](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
