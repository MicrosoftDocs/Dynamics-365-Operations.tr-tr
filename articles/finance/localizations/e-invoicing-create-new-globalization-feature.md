---
title: Genelleştirme özelliği oluşturma
description: Bu konuda, Genelleştirme özelliklerinin nasıl oluşturulacağı açıklanmaktadır.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94038b0eb412632c348081bbf467f44310d9e955
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603039"
---
# <a name="create-a-globalization-feature"></a>Genelleştirme özelliği oluşturma

[!include [banner](../includes/banner.md)]

Sıfırdan elektronik faturalama özelliği oluşturabilir veya mevcut bir özellik üzerine temellendirebilirsiniz. Sıfırdan özellik oluşturduğunuzda, Elektronik raporlama (ER) bileşenlerini ve özellik kurlumu ve uygulama kurulumu ayrıntıları gibi diğer bileşenleri el ile eklemeniz gerekir. Varolan bir özelliği temel alan bir özellik oluşturduğunuzda, yeni özellik tüm temel özelliklerin yapılandırmalarını ve parametrelerini devralır. Temel özellikten yeni özelliğe nelerin kopyalanacağını gözden geçirebilirsiniz.

## <a name="create-a-feature-from-scratch"></a>Sıfırdan özellik oluşturma

Bu bölümde, iş senaryolarınız Genel deponuzda kullanıma hazır yapılandırılabilir Genelleştirme özelliği olmadığında bir elektronik faturalama özelliğinin nasıl oluşturulacağı açıklanmaktadır.

Elektronik faturalama özelliği oluşturmak için aşağıdaki adımları izleyin.

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ekle**'yi seçin ve açılan iletişim kutusunda **Yeni özellik** seçeneğini belirleyin.
4. Elektronik faturalama özelliği için bir ad ve açıklama girin.
5. **Özellik oluştur**'u seçin. Yeni özelliğin ilk sürümü, sayfanın sağ tarafında görüntülenir ve durumu **Taslak** olarak gösterilir.

    Ardından, ER yapılandırması ve özellik kurulumları eklemelisiniz. Yeni veya varolan ER biçimi yapılandırmalarını ekleyebilmek için, bunların yerel RCS deposunda bulunduğundan emin olun.

6. Üzerinde çalıştığınız elektronik faturalama özelliğini seçin.
7. **Yapılandırmalar** sekmesinde, **Ekle**'yi seçin.
8. **Yapılandırmalar** kılavuzunda, işleme ardışık düzeni için gerekli olan konfigürasyon konfigürasyonlarına göz atın ve bunları seçin (örneğin, elektronik fatura dosyaları oluşturmak veya harici web hizmetlerinden gelen yanıtları işlemek için).
9. **Tamam**'ı seçin. Artık, işlem ardışık düzenin eylemleriyle ilgili yapılandırmaları kullanabilirsiniz. Daha fazla bilgi için bkz. [Yapılandırmalarla çalışma](e-invoicing-work-configurations.md).
10. Elektronik faturalama özellik kurulumu eklemek için, **Yeni özellik** sayfasındaki **Ayarlar** sekmesinde oluşturun. Daha fazla bilgi için bkz. [Özellik kurulumlarıyla çalışma](e-invoicing-feature-setup.md).
11. Kurulumu tamamlayın ve elektronik faturalama özelliğini hizmet ortamına dağıtın. Daha fazla bilgi için bkz. [Genelleştirme özelliğini tamamlama, yayımlama ve dağıtma](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Mevcut fatura modelinden türetilen dosya biçimi yapılandırmaları oluşturma

ER konfigürasyonları oluşturmak zorunda değilseniz ancak varolan sürümleri temel olarak yeniden kullanabiliyorsanız bu bölümü atlayabilirsiniz.

Bu yordamda, oluşturmak istediğiniz yeni elektronik faturalama özelliği için gerekli olan dosya biçimi yapılandırmalarını oluşturma açıklanmaktadır. Elektronik fatura dosya biçimi yapılandırmasını ve yeni elektronik faturalama özelliği için gerekebilecek diğer dosya biçimi yapılandırmalarını oluşturabilirsiniz.

1. RCS hesabınızda oturum açın.
2. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Fatura modelini** seçin veya Brezilya için **Mali model**'i seçin.
4. **Yapılandırma oluştur**'u seçin ve ardından açılır iletişim kutusunda, **Veri modeli faturasına dayalı biçim** seçeneğini belirleyin.
5. Biçim yapılandırması için bir ad ve açıklama girin.
6. **Biçim türü** alanında, dosya uzantısı türünü seçin.
7. **Veri modeli tanımı** alanında, biçiminizin eşleneceği kök yapıyı seçin. Örneğin, **InvoiceCustomer**, müşteri fatura biçimleri için kullanılır.
8. **Yapılandırma oluştur**'u seçin.
9. Yeni biçim yapılandırmasını seçin.
10. **Tasarımcı**'yı seçin ve dosya biçimi özelliklerini karşılaması için dosya düzenini yapılandırmak üzere Biçim tasarımcısı aracını kullanın.
11. Sayfayı kapatın.
12. **Sürümler** sekmesinde, **Durumu değiştir** \> **Tamamla**'yı seçin.
13. Biçim yapılandırmasını Genel depoda yayımlamak için **Durumu değiştir** \> **Paylaş**'ı seçin.

Yapılandırma, Elektronik faturalama hizmeti tarafından tüketilmeden önce yeni dosya biçimi yapılandırmalarının Microsoft etki alanıyla paylaşılması gerekir.

1. Üzerinde çalıştığınız biçim yapılandırmasını seçin. Yapılandırmanın durumu, **Paylaşılan** olmalıdır.
2. **Sürümler** sekmesinde, **Gelişmiş paylaşım** \> **Genel depo**'yu seçin.
3. **Paylaşılan** sekmesinde **Kuruluş**'u seçin.
4. **Parametreler** alanında, biçim yapılandırmasını Microsoft etki alanıyla paylaşmak için **microsoft.com** adresini girin.
5. **Tamam**'ı seçin.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Varolan bir özelliği temel alan özellik oluşturma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Yapılandırma sağlayıcısı** alanında, etkin yapılandırma sağlayıcınızın seçildiğinden emin olun. Bu şekilde, yeni elektronik faturalama özelliği, oluşturulduktan sonra listesinde görüntülenir. Etkin yapılandırma sağlayıcınız seçili değilse, yeni özellik filtreyle liste dışı bırakılır.
4. **Ekle**'yi seçin ve açılan iletişim kutusunda **varolan sürüme bağlı** seçeneğini belirleyin.
5. Özellik için bir ad ve açıklama girin.
6. **Temel özellik** alanında, özelliğin temel sürümünü seçin.
7. **Özellik oluştur**'u seçin. Özellik oluşturulur ve **Taslak** durumuna sahip olur.
8. Güncelleştirmelerin gerekli olup olmadığını belirlemek için özellik bileşenlerini gözden geçirin:

    - ER biçimlerini ve bunların, özellik sürümü için biçim eşlemeleriyle olan bağlamasını özelleştirmeniz olasılığına karşı konfigürasyonları gözden geçirin.
    - Özellik sürümü için **Eylemler** sekmesini, **uygulanabilirlik kuralları** sekmesini veya **değişkenler** sekmesini özelleştirmeniz gerekebileceği için kurulumu gözden geçirin.

9. Kurulumu tamamlayın ve elektronik faturalama özelliğini hizmet ortamına dağıtın. Daha fazla bilgi için bkz. [Genelleştirme özelliğini tamamlama, yayımlama ve dağıtma](e-invoicing-complete-publish-deploy-globalization-feature.md).
