---
title: Azure depolama hesabı ve bir anahtar kasası oluşturma
description: Bu konu, bir Azure depolama hesabı ve anahtar kasası oluşturma yöntemini açıklamaktadır.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5a883011bbff6d82504497d739c07f1ada9e5f69
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2020
ms.locfileid: "4448991"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure depolama hesabı ve bir anahtar kasası oluşturma

[!include [banner](../includes/banner.md)]



Elektronik faturalama eklentisi servisi tüm iş verilerinizi şirketinize ait Microsoft Azure kaynaklarda saklamaktan sorumlu olur. Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gerekli olan ve bu eklenti tarafından oluşturulan ve yalnızca eklenti tarafından oluşturulmuş tüm iş verilerine erişmesini sağlamak için iki ana Azure kaynağı oluşturmanız gerekir:

- Elektronik faturaları depolamak için bir Azure depolama hesabı (Blob depolama)
- Sertifikaları ve depolama hesabının Tekdüzen Kaynak tanımlayıcısı'nı (URI) depolamak için bir Azure Anahtar Kasası

> [!NOTE]
> Adanmış bir Anahtar Kasası kaynağı ve müşteri Blob depolaması özel olarak Elektronik faturalama eklentisi ile kullanılmak üzere ayrılmalıdır.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları tamamlayabilmek için aşağıdaki görevlerin tamamlanmış olması gerekir:

- Azure'da anahtar kasası kaynağı oluşturun. Daha fazla bilgi için bkz. [Azure Anahtar Kasası hakkında](https://docs.microsoft.com/azure/key-vault/general/overview).
- Bir Azure depolama hesabı (Blob deposu) oluşturun. Daha fazla bilgi için bkz [Azure Depolama Hesabını sürdürme](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Genel bakış

Bu konuda, iki ana adımı tamamlayacaksınız:

- Depolama hesabı URI'sini almak için Azure depolama hesabını ayarlayın.
- Depolama hesabı URI'sini depolamak için anahtar kasasını ayarlayın.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Depolama hesabı URI'sini almak için Azure depolama hesabını ayarlama

1. Elektronik faturalama eklentisi ile kullanmayı planladığınız depolama hesabını açın.
2. **Blob hizmeti** \> **Kapsayıcılar** öğesine gidin ve yeni bir kapsayıcı oluşturun.
3. Kapsayıcı için bir ad girin ve **Ortak erişim düzeyi** alanını **Özel (anonim erişim yok**) olarak ayarlayın.
4. Kapsayıcıyı açın ve **Ayarlar \> Erişim ilkesi**'ne gidin.
5. Depolanan erişim ilkesi eklemek için **İlke ekle**'yi seçin.
6. **Tanımlayıcı** ve **İzinler** alanlarını uygun şekilde ayarlayın. **İzinler** alanında, tüm izinleri seçmelisiniz.

    ![Blob depolama izni verme](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Başlangıç ve bitiş tarihlerini girin. Bitiş tarihi gelecekte olmalıdır.
8. İlkeyi kaydetmek için **Tamam**'ı seçin ve sonra değişikliklerinizi kapsayıcıya kaydedin.
9. Depolama hesabına dönün ve **Depolama Gezgini (Önizleme)** ögesini açın.
10. Kapsayıcıyı sağ tıklayın ve sonra da **Paylaşılan Erişim İmzasını Al**'ı seçin.
11. **Paylaşılan Erişim İmzası** iletişim kutusunda, değeri **URI** alanına kopyalayın ve saklayın. Bu değer sonraki yordamda kullanılacak ve *paylaşılan erişim imza URI*'si olarak anılacaktır.

    ![URI değerini seçme ve kopyalama](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Depolama hesabı URI'sini depolamak için anahtar kasasını ayarlama

1. Elektronik faturalama eklentisi ile kullanmayı planladığınız anahtar kasasını açın.
2. **Ayarlar** \> **Gizli anahtarlar** ögesine gidin ve yeni bir gizli anahtar oluşturmak için **Oluştur/içe aktar**'ı seçin.
3. **Gizli anahtar oluştur** sayfasında **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.
4. Gizli anahtarın adını girin. Bu ad, Regulatory Configuration Service (RCS) içindeki servisin kurulumu sırasında kullanılacaktır ve *anahtar kasası gizli anahtar adı* olarak anılacak.
5. **Değer** alanında, **Paylaşılan Erişim İmza URI'si** ögesini seçin ve **Oluştur**'u seçin.
6. Elektronik faturalama eklentisini, oluşturduğunuz gizli anahtara doğru güvenli erişim düzeyine vermek için erişim ilkesini ayarlayın. **Ayarlar \> Erişim ilkesi** ögesine gidin ve **Erişim ilkesi ekle**'yi seçin.
7. **Get** ve **List** işlemleri için gizli anahtar izinlerini ayarlayın.

    ![Servis erişimi verme](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. **Get** ve **List** işlemleri için sertifika izinlerini ayarlayın.

    ![Sertifika izni verme](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. **Sorumlu** iletişim kutusunda, **Elektronik faturalama eklentisi** ekleyerek sorumluyu seçin.
10. **Ekle**'yi seçin ve **Anahtar Kasa değişikliklerini kaydet**'i seçin.
11. **Genel Bakış** sayfasında, anahtar kasası için **DNS adı** değerini kopyalayın. Bu değer, servisin kurulumu sırasında, RCS'de kullanılır ve *anahtar kasa URI*'si olarak anılacaktır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]