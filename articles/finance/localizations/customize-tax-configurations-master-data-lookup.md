---
title: Ana veri arama için vergi konfigürasyonlarını özelleştirme
description: Bu konu, ana veri arama işlevini genişletmek için vergi konfigürasyonlarının nasıl özelleştirileceğini açıklamaktadır.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689142"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Ana veri arama için vergi konfigürasyonlarını özelleştirme

[!include [banner](../includes/banner.md)]

Ana veri arama işlevini genişletmek için vergi konfigürasyonlarını özelleştirmek için bu konudaki adımları izleyin.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Microsoft tarafından sağlanan bir vergi yapılandırmasını içe aktarma

1. Regulatory Configuration Service'de (RCS), **Elektronik raporlama** çalışma alanında **Microsoft** konfigürasyon sağlayıcısını seçin.
2. **Depolar**'ı seçin.
3. **Genel**'i seçin ve **Aç**'ı seçin.
4. **Vergi Hesaplama Konfigürasyonu** gibi bir vergi konfigürasyonu seçin ve **Sürümler** sekmesinde bir sürüm seçin.
5. **İçe aktar**'ı seçin.

> [!NOTE]
> Varsayılan olarak, Dataverse model eşleme içe aktarılır. Konfigürasyon içe aktarma işlemi sırasında uyarı iletileri alıyorsanız, Dataverse'de sanal varlıkları etkinleştirin. Daha fazla bilgi için bkz. [Dataverse sanal varlıklarını etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Özelleştirilmiş bir veri modeli yapılandırması oluşturun

1. **Elektronik raporlama** çalışma alanında, **Vergi konfigürasyonları**'nı seçin ve sonra genişletilecek veri modeli konfigürasyonunu seçin. Örneğin, **Vergi Hesaplama Veri Modeli**'ni seçin.
2. **Yapılandırma oluştur**'u seçin.
3. **Ad: Veri Hesaplama Veri Modeli, Microsoft'tan türetilen vergilendirilebilir belge modeli**'ni seçin.
4. **Ad** alanına **Özelleştirme veri modeli**'ni girin.
5. **Yapılandırma oluştur**'u seçin.

## <a name="create-customized-reference-models"></a>Özelleştirilmiş referans modelleri oluşturma

1. **Vergi konfigürasyonları** sayfasında, **Özelleştirme veri modeli**'ni seçin ve sonra **Tasarımcı**'yı seçin.
2. Modül için üç nokta düğmesini (**...**) seçin ve sonra **Referans modeli** görünümünü seçin.

    [![Referans modeli.](./media/pic2.png)](./media/pic2.png)

3. Özelleştirilmiş referans modelini oluşturun. Özelleştirilmiş model, bir kök modeldir. Özelleştirilmiş varlık, bir kayıt listesidir. Özelleştirilmiş alan, aramada kullanmak istediğiniz dize alanıdır. Bu alanlara istediğiniz şekilde daha fazla ekleyebilirsiniz.
4. Modül için üç nokta düğmesini (**...**) seçin ve sonra **Vergilendirilebilir belge** görünümünü seçin.
5. Özelleştirilmiş referans modeline bağlanacak özniteliği seçin. Örneğin, **Özelleştirilmiş özniteliği** seçin ve şu adımları izleyin:

    1. **Referans modelini seç** öğesini belirleyin.
    2. **Özelleştirilmiş model**'i seçin ve **Tamam**'ı seçin. Referans modeli adı, **Doğal anahtar** alanının değeriyle güncelleştirilir.

        [![Referans modeli iletişim kutusunu seçin.](./media/pic5.png)](./media/pic5.png)

    3. **Kaydet** i seçin ve sonra **Tamamla**'yı seçin.

## <a name="create-a-customized-model-mapping-configuration"></a>Özelleştirilmiş bir veri modeli eşlemesi oluşturun

1. **Elektronik raporlama** çalışma alanında, **Vergi konfigürasyonları**'nı seçin ve sonra **Dataverse model eşleme** konfigürasyonunu seçin.
2. **Model eşleme için varsayılan** alanında **Hayır**'ı seçin.
3. **Yapılandırma oluştur**'u seçin.
4. **Ad: Dataverse Model Eşleme, Microsoft'tan türetilen vergilendirilebilir model eşleme**'yi seçin.
5. **Ad** alanına **Özelleştirme model eşlemesi**'ni girin.
6. **Hedef model** alanında, **Özelleştirme veri modeli** veri modelini seçin.
7. **Yapılandırma oluştur**'u seçin.

    [![Yapılandırma oluşturma açılan iletişim kutusu.](./media/pic6.png)](./media/pic6.png)

8. **Özelleştirme modeli eşleme**'yi seçin ve **Bağlı uygulama** alanını, [Ana veri arama için bir ortam ayarlamada](tax-service-set-up-environment-master-data-lookup.md), 8. adımda oluşturulan bağlantıya ayarlayın.
9. **Model eşleme için varsayılan** alanını **Evet** olarak ayarlayın.

## <a name="create-customized-model-mappings"></a>Özelleştirilmiş model eşleştirmeleri oluştur

1. **Vergi konfigürasyonları** sayfasında, **Özelleştirme modeli eşlemesi**'ni seçin.
2. **Tasarımcı**'yı seçin ve **Özelleştirme Modeli**'ni seçin.

    [![Özelleştirme Modeli.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Bir model eşlemesini, Dataverse varlığına eşleyin

1. **Model eşleme tasarımcısı** sayfasında, **Özelleştirme Modeli**'ni seçin ve sonra **Tasarımcı**'yı seçin.
2. **Veri kaynağı türleri** ağacında, **Dataverse Tablo**'yu seçin.
3. **Veri kaynakları** sekmesinde **Kök ekle**'yi seçin.
4. **Ad** alanına, **Özelleştirilmiş Dataverse** girin.
5. İkinci **Ad** alanında bir varlık seçin.
6. **Tamam**'ı seçin.

    [!['Tablo' veri kaynağı özellikleri iletişim kutusu.](./media/pic9.png)](./media/pic9.png)

7. **Özelleştirilmiş Dataverse** ve **Özelleştirilmiş varlık**'ı seçin ve sonra **Bağla**'yı seçin.

    [![Özelleştirilmiş Dataverse ve Özelleştirilmiş varlık bağlama.](./media/pic10.png)](./media/pic10.png)

8. **Özelleştirilmiş Dataverse** ve **Özelleştirilmiş alan** altında bir alan seçin ve sonra **Bağla**'yı seçin.

    [![Özelleştirilmiş Dataverse ve Özelleştirilmiş alan bağlama.](./media/pic11.png)](./media/pic11.png)

9. **Kaydet** i seçin ve sonra **Tamamla**'yı seçin.

## <a name="create-a-customized-tax-configuration"></a>Özelleştirilmiş bir vergi yapılandırması oluşturun

1. **Elektronik raporlama** çalışma alanında, **Vergi konfigürasyonları**'nı seçin ve sonra **Vergi Hesaplama Konfigürasyonu**'nu seçin.
2. **Yapılandırma oluştur**'u seçin.
3. **Ad: Vergi Hesaplama Konfigürasonu, Microsoft'tan türetilmiş vergi hizmeti konfigürasyonu**'nu seçin.
4. **Ad** alanına **Özelleştirme konfigürasyonu**'nu girin.
5. **Yapılandırma oluştur**'u seçin.
6. **Özelleştirme konfigürasyonu**'nu seçin ve **Tasarımcı**'yı seçin.
7. **Veri modeli** alanında, **Özelleştirme veri modeli**'ni seçin.
8. **Veri modeli sürümü** alanında, karşılık gelen veri modeli sürümünü seçin.

    [![Özellikler bölümü.](./media/pic13.png)](./media/pic13.png)

9. **Tamamlandı**'yı seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
