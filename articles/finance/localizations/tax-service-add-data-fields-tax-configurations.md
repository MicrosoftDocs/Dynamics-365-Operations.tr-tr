---
title: Vergi yapılandırmalarına veri alanları Ekleme
description: Bu konu, veri alanları ekleyerek vergi yapılandırmalarının nasıl özelleştirileceğini açıklamaktadır.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 56b2eae37738ff6a12226671c386e2dd63c380bd4dca1554ef2d1cad0b75faaa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725953"
---
# <a name="add-data-fields-in-tax-configurations"></a>Vergi yapılandırmalarına veri alanları Ekleme

[!include [banner](../includes/banner.md)]

Bu konu [vergi tümleştirmesinde eklenen veri alanlarını](tax-service-add-data-fields-tax-integration-by-extension.md) kullanarak vergi yapılandırmalarının nasıl özelleştirileceğini açıklamaktadır.

## <a name="customize-the-tax-data-model"></a>Vergi veri modeli yapılandırmasını özelleştirme

1. Microsoft Dynamics 365 Finance'te **Elektronik raporlama** \> **Vergi Yapılandırmaları**'na gidin.
2. Yapılandırma ağacında, **vergi veri modeli-Avrupa**'yı seçin. Ardından Eylem bölmesinden **Yapılandırma oluştur**'u seçin.
3. Açılan iletişim kutusunda, **Vergi veri modeli -- Avrupa, Microsoft adından türetilen vergiye tabi belge modelini** seçin, yeni vergi veri modeli için bir ad girin ve sonra **Yapılandırma oluştur**'u seçin.
4. Oluşturduğunuz vergi veri modelini seçin ve sonra eylem bölmesinde **tasarımcı**'yı seçin.
5. Veri modeli ağacını genişletin, **Satırlar**'ı seçin ve sonra **yeni**'yi seçin.
6. **Düğüm oluştur** iletişim kutusunda bir ad girin, öğe türünü belirtin ve sonra **Ekle**'yi seçin.
7. Gerekli sütunları ekleyin.
8. Eylem Bölmesinde, **Kaydet**'i ve sonra **Tamamla**'yı seçin.
9. Sayfayı kapatın ve vergi veri modelinizin tamamlanan sürümünü görüntüleyin.

## <a name="customize-the-tax-configuration"></a>Vergi yapılandırmasını özelleştirme

1. Finance'te **Elektronik raporlama** \> **Vergi Yapılandırmaları**'na gidin.
2. Yapılandırma ağacında, **vergi yapılandırması -- Avrupa**'yı seçin. Ardından Eylem bölmesinden **Yapılandırma oluştur**'u seçin.
3. Açılan iletişim kutusunda, **Vergi Yapılandırması -- Avrupa, Microsoft adından türetilen vergi hizmeti yapılandırmasını** seçin, yeni vergi yapılandırması için bir ad girin ve sonra **Yapılandırma oluştur**'u seçin.
4. Oluşturduğunuz vergi yapılandırmasını seçin ve sonra eylem bölmesinde **tasarımcı**'yı seçin.
5. **Özellikler** bölümünde, **veri modeli** alanında, önceden oluşturduğunuz özelleştirilmiş vergi veri modelini seçin.
6. **Veri modeli sürümü** alanında, vergi veri modelinin tamamlanmış sürümünü seçin.
7. **Ekle**'yi seçin ve gerekli vergi ölçümlerini ekleyin.
8. Eylem Bölmesinde, **Kaydet**'i ve sonra **Tamamla**'yı seçin.
9. Sayfayı kapatın ve vergi yapılandırmanızın tamamlanan sürümünü görüntüleyin.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Özelleştirilmiş vergi yapılandırmasındaki vergi özelliklerini Uygulama

1. Regulatory Configuration Services'te (RCS) **Genelleştirme Özellikleri** \> **Vergi**'ye gidin.
2. **Ekle**'yi seçin, yeni özellik hakkındaki bilgileri girin ve sonra **Oluştur** özelliğini seçin.
3. **Sürümler** sekmesinde özelliği seçin ve sonra **Düzenle**'yi seçin.
4. **Genel** sekmesinde, **Yapılandırma sürümü** alanında, özelleştirilmiş vergi yapılandırmasını ve sürümünü seçin.
5. **Sütunları Yönet** iletişim kutusunda, özelleştirilmiş vergi ölçümünüzde olmasını istediğiniz başlık ve satır sütunlarını seçin ve bunları **Seçilen sütunlar** listesine eklemek için sağ ok düğmesini seçin.
