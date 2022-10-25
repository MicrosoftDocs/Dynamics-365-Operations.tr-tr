---
title: Vergi hesaplamalarını içeri ve dışarı aktarma
description: Bu makale, vergi hesaplama hizmetinin içeri aktarma ve dışarı aktarma işlevi hakkında bilgi sağlar.
author: Kai-Cloud
ms.date: 10/17/2022
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
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690246"
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

## <a name="import-feature-demo-data"></a>Özellik tanıtım verilerini içe aktarma

Özellik tanıtım verilerini içe aktarmak için aşağıdaki adımları izleyin.

1. [RCS](https://marketing.configure.global.dynamics.com/)'de oturum açın
2. **Globalleştirme özellikleri** çalışma alanında **Özellikler**'i seçin ve sonra **Vergi hesaplama** kutucuğunu seçin.
3. **İçe aktar**'ı seçin ve ardından **Özelliği Genel depodan içe aktar** sayfasında **Eşitle** seçeneğini belirleyin. 
4. Tabloda **tax-calculation-feature-demo-data** özelliğini seçin ve ardından **İçe aktar** seçeneğini belirleyin.
5. İçe aktarılan özellikte tanımlanan vergi kodlarını, gruplarını ve uygulanabilirlik kurallarını gözden geçirmek için **Görüntüle**'yi seçin.
6. Finance'te **DEMF** tüzel kişiliğine geçin ve ardından **Vergi** \> **Kurulum** \> **Vergi konfigürasyonu** \> **Vergi hesaplama parametreleri** bölümüne gidin.
7. **Genel** sekmesinde **Vergi Hesaplama Hizmetini Etkinleştir**'i seçin.
8. **Özellik kurulumu adı** alanında **tax-calculation-feature-demo-data** seçeneğini belirleyin.
9. Yeni tanıtım vergi kodları için **Kapatma dönemi** ve **Genel muhasebe deftere nakil grubu** seçin ve ardından **Onayla** seçeneğini belirleyin.
10. **Kaydet**'i seçin.

> [!NOTE]
> **tax-calculation-feature-demo-data** tanıtım özelliği, özellik sürümü **40.54.234**'ü temel alır ve **DEMF** tanıtım tüzel kişiliği için tasarlanmıştır. Finance ve RCS'nin sürüm 10.0.26 veya üstüne yükseltildiğinden emin olun.
