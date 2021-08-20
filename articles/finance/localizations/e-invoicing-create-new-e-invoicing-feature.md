---
title: Yeni bir Elektronik faturalama özelliği oluşturma
description: Bu konuda, ülkeniz veya bölgenizde kullanıma hazır yapılandırılabilir özellik olmadığında yeni bir Elektronik faturalama özelliğinin nasıl oluşturulacağı açıklanmaktadır.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744947"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Yeni bir Elektronik faturalama özelliği oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, ülkeniz veya bölgenizde kullanıma hazır yapılandırılabilir özellik olmadığında yeni bir Elektronik faturalama özelliğinin nasıl oluşturulacağı açıklanmaktadır.

Yeni bir Elektronik faturalama özelliği oluşturmak için şu görevleri tamamlayın:

1. Sağlanan fatura modeli yapılandırmasını kullanarak ve oluşturmak istediğiniz özellik için mevcut fatura eşlemesinden faydalanarak yeni bir dosya biçimi yapılandırması oluşturun.
2. Dosya biçimi yapılandırmalarını Elektronik faturalama özelliği yapılandırmalarına ekleyin.
3. Elektronik faturalama özelliği kurulumunu oluşturun.
4. Yeni Elektronik faturalama özelliğini tamamlayın ve bunu kuruluşunuz için Genel depoda yayımlayın.
5. Yeni Elektronik faturalama özelliğini Servis ortamına dağıtın.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Mevcut fatura modelinden türetilen yeni dosya biçimi yapılandırmaları oluşturma

Bu yordamda, oluşturmak istediğiniz yeni Elektronik faturalama özelliği için gerekli olan dosya biçimi yapılandırmalarını oluşturacaksınız. Elektronik fatura dosya biçimi yapılandırmasını ve yeni Elektronik faturalama özelliği için gerekebilecek diğer dosya biçimi yapılandırmalarını oluşturabilirsiniz.

Bu yordama başlamadan önce Regulatory Configuration Service (RCS) hesabınızda oturum açın.

1. Microsoft Dynamics 365 Finance'te, **Elektronik raporlama** çalışma alanında, **Microsoft** yapılandırma sağlayıcısı için **Depolar**'ı seçin.
2. **Genel**'i seçin, **Aç** seçeneğini belirleyin ve ardından sol bölmede **Fatura modeli** yapılandırmasını seçin.

    > [!IMPORTANT]
    > Brezilya için, bunun yerine **Mali belgeler** modeli yapılandırmasını seçin.

3. **Yapılandırmalar** sekmesinde, **İçeri Aktar**'ı seçin.
4. Sayfayı kapatın.
5. Sayfayı kapatın.
6. **Raporlama yapılandırmaları** kutucuğunu ve ardından içeri aktardığınız fatura modelini seçin.
7. **Yapılandırma oluştur**'u seçin ve ardından **Fatura bağlam modeline dayalı biçim** seçeneğini belirleyin.
8. Biçim yapılandırması için bir ad ve açıklama girin.
9. **Biçim türü** alanında, dosya uzantısı türünü seçin.
10. **Yapılandırma oluştur** seçeneğini belirleyin ve ardından oluşturduğunuz biçim yapılandırmasını seçin.
11. **Tasarımcı**'yı seçin ve dosya biçimi özelliklerini karşılaması için dosya düzenini yapılandırmak üzere Biçim tasarımcısı aracını kullanın.
12. Sayfayı kapatın.
13. **Sürümler** sekmesinde, **Durumu değiştir** \> **Tamamla**'yı seçin.
14. Biçim yapılandırmasını Genel depoda yayımlamak için **Durumu değiştir** \> **Paylaş**'ı seçin.

Yapılandırma, Elektronik faturalama hizmeti tarafından tüketilmeden önce yeni dosya biçimi yapılandırmasının Microsoft etki alanıyla paylaşılması gerekir.

1. Üzerinde çalıştığınız biçim yapılandırmasını seçin. Yapılandırmanın durumu, **Paylaşılan** olmalıdır.
2. **Sürümler** sekmesinde, **Gelişmiş paylaşım** \> **Genel depo**'yu seçin.
3. **Paylaşılan** sekmesinde **Kuruluş**'u seçin.
4. **Parametreler** alanında, biçim yapılandırmasını Microsoft etki alanıyla paylaşmak için **Microsoft.com** adresini girin.
5. **Tamam**'ı seçin.

## <a name="create-the-new-electronic-invoicing-feature"></a>Yeni Elektronik faturalama özelliğini oluşturma

1. RCS'de, **Genelleştirme özellikleri** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Ekle**'yi seçin ve ardından **Yeni özellik** seçeneğini belirleyin.
3. Elektronik faturalama özelliği için bir ad ve açıklama girin.
4. **Özellik oluştur**'u seçin.

## <a name="add-electronic-invoicing-feature-configurations"></a>Elektronik faturalama özelliği yapılandırmaları ekleme

1. Üzerinde çalıştığınız Elektronik faturalama özelliğini seçin.
2. **Yapılandırmalar** sekmesinde, **Ekle**'yi seçin.
3. **Yapılandırmalar** ızgarasında, elektronik fatura dosyası oluşturmak için Elektronik faturalama özelliğinizin gerektirdiği dosya biçimi yapılandırmalarına göz atıp seçin.
4. **Tamam**'ı seçin.

## <a name="add-electronic-invoicing-feature-setups"></a>Elektronik faturalama özelliği kurulumları ekleme

1. **Kurulumlar** sekmesinde, **Ekle**'yi seçin ve ardından **Özel kurulum** seçeneğini belirleyin.
2. Özellik kurulumu için bir ad ve açıklama girin.
3. **Kurulum türü** alanında, **İşleme ardışık düzeni**'ni seçin.
4. **Oluştur**'u seçin.
5. Üzerinde çalıştığınız kurulumu seçin ve ardından **Düzenle** seçeneğini belirleyin.
6. **İşleme ardışık düzeni** sekmesinde, ardışık düzen eylemi eklemek için **Yeni**'yi seçin. Ardışık düzenler hakkında daha fazla bilgi için bkz. [Eylemler](e-invoicing-configuration-rcs.md#actions).
7. **Uygulanabilirlik kuralları** sekmesinde, uygulanabilirlik kuralı yan tümceleri eklemek için **Yeni**'yi seçin. Uygulanabilirlik kuralları hakkında daha fazla bilgi için bkz. [Uygulanabilirlik kuralları](e-invoicing-configuration-rcs.md#applicability-rules).
8. **Değişkenler** sekmesinde, gerektiğinde değişken eklemek için **Yeni**'yi seçin.
9. **Kaydet**'i seçin ve ardından yapılandırmanın tutarlılığını denetlemek için **Doğrula** seçeneğini belirleyin.
10. Sayfayı kapatın.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Elektronik faturalama özelliğini Servis ortamına dağıtma

Bu görevi tamamlama hakkında bilgi için bkz. [Elektronik faturalama özelliğini Servis ortamına dağıtma](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Elektronik faturalama özelliğini bağlı uygulamaya dağıtma

Bu görevi tamamlama hakkında bilgi için bkz. [Uygulama kurulumunu yapılandırma](e-invoicing-get-started.md#configure-the-application-setup) ve [Elektronik faturalama özelliğini Bağlı uygulamaya dağıtma](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
