---
title: Vergi hesaplamalarını içeri ve dışarı aktarma
description: Bu makale, vergi hesaplama hizmetinin içeri aktarma ve dışarı aktarma işlevi hakkında bilgi sağlar.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 9daee683763d7cb0eb9573497eb4e20cba9b1863
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855187"
---
# <a name="import-and-export-tax-calculations"></a>Vergi hesaplamalarını içeri ve dışarı aktarma

Bu makale, vergi hesaplama hizmetinin içeri aktarma ve dışarı aktarma işlevi hakkında bilgi sağlar. Bu işlevsellik, esnek ve verimli bir yapılandırma deneyimi sağlamaya yardımcı olur.

## <a name="import-and-export-tax-codes"></a>Vergi kodlarını içeri aktarma ve dışarı aktarma

### <a name="export-templates"></a>Dışarı aktarma şablonları

1. [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/) üzerinde oturum açın.
2. **Globalleştirme özellikleri** çalışma alanında **Özellikler**'i seçin ve sonra **Vergi hesaplama** kutucuğunu seçin.
3. Var olan bir özellik seçin veya [yeni bir özellik oluşturun](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. **Sürümler** kılavuzunda **Düzenle**'yi seçin.
5. **Vergi hesaplama** özelliği sayfasında, [yapılandırma sürümünü](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) ayarlayın.
6. **Vergi kodları** sekmesinde **İçeri Aktar**'ı seçin.
7. **TaxCodesTemplate.zip** dosyasını indirmek için **Vergi kodunu dışarı aktar şablonu**'nu seçin.
8. **TaxCodesTemplate.zip** dosyasını açın. Vergi kodu şablonları, **Hesaplama kaynağı** değerine göre ayrı ayrı sıkıştırılır.
9. Aşağıdaki virgülle ayrılmış değerler (CSV) dosyalarını almak için **Net tutara göre.zip** dosyasını açın:

    - **TaxCode.csv** – Vergi kodlarını girin.
    - **TaxLimit.csv** – Her vergi kodu için vergi sınırlarını girin.
    - **TaxRate.csv** – Her vergi kodu için vergi oranlarını girin.

> [!NOTE]
> Varsayılan olarak **Örnek** vergi kodu girişleri şablonlarda kullanılabilir. **Örnek** vergi kodu CSV dosyalarından kaldırılmazsa özelliğe içeri aktarılır.

### <a name="import-tax-codes"></a>Vergi kodlarını içeri aktarma

Şablondaki **Örnek** vergi kodunu vergi hesaplama özelliğinize içeri aktarmak için bu adımları izleyin.

1. RCS'de, **Vergi hesaplama** özelliği sayfasında, **Vergi kodları** sekmesinde **İçeri Aktar**'ı seçin.
2. **Göz At**'ı seçin, **TaxCode.csv** dosyasını bulup seçin ve **Hedef tablo** alanında **Vergi kodu**'nu seçin.
3. Vergi kodunu içeri aktarmak için **Tamam**'ı seçin.
4. **TaxRate.csv** dosyasını bulup seçin ve **Hedef tablo** alanında **Vergi oranı**'nı seçin.
5. Vergi oranını içeri aktarmak için **Tamam**'ı seçin.
6. **TaxLimit.csv** dosyasını bulup seçin ve **Hedef tablo** alanında **Vergi sınırı**'nı seçin.
7. Vergi sınırını içeri aktarmak için **Tamam**'ı seçin.

Ayrıca, üç CSV dosyasını da içeren zip dosyasını doğrudan içeri aktarabilirsiniz. Bu şekilde, içeri aktarma işlemini hızlı ve kolay bir şekilde tamamlayabilirsiniz.

1. RCS'de, **Vergi hesaplama** özelliği sayfasında, **Vergi kodları** sekmesinde **İçeri Aktar**'ı seçin.
2. **Göz At**'ı seçin, **Net Tutara Göre.zip** dosyasını bulup seçin ve sonra **Tamam**'ı seçin.

### <a name="export-tax-codes"></a>Vergi kodlarını dışarı aktarma

1. RCS'de, **Vergi hesaplama** özelliği sayfasında, **Vergi kodları** sekmesinde **Dışarı Aktar**'ı seçin.

    **Dışarı Aktar** düğmesi, **Vergi kodları** kılavuzunda en az bir vergi kodu olduğunda kullanılabilir.

2. Özelliğin tüm vergi kodlarını bir zip dosyasına dışarı aktarmak için **Tamam**'ı seçin.

> [!NOTE]
> Vergi kodlarını ilgili özelliğe içeri aktarmak için dışarı aktarılan dosyayı şablon olarak kullanın.

## <a name="import-and-export-applicability-rules"></a>Uygulanabilirlik kurallarını içeri aktarma ve dışarı aktarma

### <a name="export-applicability-rules"></a>Uygulanabilirlik kurallarını dışarı aktarma

1. [RCS](https://marketing.configure.global.dynamics.com/)'de oturum açın
2. **Globalleştirme özellikleri** çalışma alanında **Özellikler**'i seçin ve sonra **Vergi hesaplama** kutucuğunu seçin.
3. Var olan bir özellik seçin veya [yeni bir özellik oluşturun](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. **Sürümler** kılavuzunda **Düzenle**'yi seçin.
5. **Vergi hesaplama** özelliği sayfasında, [yapılandırma sürümünü](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) ayarlayın.
6. **Vergi grubu uygulanabilirliği** sekmesinde, **Vergi grubu uygulanabilirliğini ayarla** kılavuzundaki satırları seçin.
7. **Microsoft Office'te aç** düğmesini seçin ve ardından **Vergi servisi dinamik uygulanabilirlik matrisi**'ni seçin.

    [![Uygulanabilirlik kurallarını Vergi hesaplama özelliği sayfasında Microsoft Excel'e dışarı aktarma.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Seçili satırları Microsoft Excel çalışma sayfasına dışarı aktarmak için **İndir**'i seçin.

### <a name="import-applicability-rules"></a>Uygulanabilirlik kurallarını içeri aktarma

İndirdiğiniz Excel çalışma sayfası, **Vergi grubu uygulanabilirliğini ayarla** kılavuzunun yapısını içerir. Yeni kuralları doğrudan çalışma sayfasına ekleyebilirsiniz. İşiniz bittiğinde, yeni kuralları **Vergi grubu uygulanabilirliğini ayarla** kılavuzuna tekrar içeri aktarmak için şu adımları izleyin.

1. Excel çalışma sayfasında, içeri aktarılacak satırları seçin ve kopyalayın.
2. RCS'de, **Vergi hesaplama** özelliği sayfasında, **Vergi grubu uygulanabilirliği** sekmesinde, **Vergi grubu uygulanabilirliğini ayarla** kılavuzunun altına boş bir kayıt eklemek için **Ekle**'yi seçin.
3. Kopyalanan satırları kılavuza yapıştırmak için **Ctrl+V** tuşlarını seçin.
4. **Kaydet**'i seçin.
