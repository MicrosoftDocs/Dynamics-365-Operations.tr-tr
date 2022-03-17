---
title: Azure portalda Azure depolama hesabı oluşturma
description: Bu konu, Elektronik faturalama için bir Azure depolama hesabı oluşturma yöntemini açıklamaktadır.
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
ms.openlocfilehash: 3d9647e234b3603ef6305ec6031a793b744bbe98
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371800"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure portalda Azure depolama hesabı oluşturma

[!include [banner](../includes/banner.md)]

Elektronik faturalama servisi tarafından oluşturulan veya işlem sırasında hizmete gelen tüm elektronik dosyalar Microsoft Azure depolama hesabı kapsayıcılarında depolanır. Elektronik faturalamanın bu kapsayıcılara erişebilmesini sağlamak için, depolama hesabının paylaşılan erişim imzası (SAS) belirtecini elektronik faturalama hizmetine sağlamanız gerekir. Ek olarak, belirtecin güvenli şekilde depolanmasını sağlamak için SAS belitrecini doğrudan sağlamadığınızdan emin olun. Bunun yerine, bunu bir Azure Key Vault içinde depolayın ve bir Azure Key Vault gizli dizisi sağlayın.

1. Elektronik faturalama servisi ile kullanmayı planladığınız depolama hesabını açın.
2. **Ayarlar** \> **Yapılandırma**'ya gidin ve **Blob genel erişimine izin ver** parametresinin **Etkin** olarak ayarlandığından emin olun.
3. **Veri depolama** \> **Kapsayıcılar**'a gidin ve yeni bir kapsayıcı oluşturun.
4. Kapsayıcı için bir ad girin ve **Ortak erişim düzeyi** alanını **Özel (anonim erişim yok**) olarak ayarlayın.
5. Yeni kapsayıcıyı açın ve **Ayarlar** \> **Erişim ilkesi**'ne gidin.
6. Depolanan erişim ilkesi eklemek için **İlke ekle**'yi seçin.
7. **Tanımlayıcı** alanını uygun şekilde ayarlayın.
8. **İzinler** alanında, tüm izinleri seçin.

    ![Ekleme ilkesi iletişim kutusundaki İzinler alanında seçilen tüm izinler.](media/e-invoicing-azure-1.png)

9. Başlangıç ve bitiş tarihlerini girin. Bitiş tarihi gelecekte olmalıdır.
10. İlkeyi kaydetmek için **Tamam**'ı seçin ve sonra değişikliklerinizi kapsayıcıya kaydedin.
11. **Ayarlar** \> **Paylaşılan erişim belirteçleri**'ne gidin ve alan değerlerini ayarlayın.
12. Başlangıç ve bitiş tarihlerini girin. Bitiş tarihi gelecekte olmalıdır.
13. **İzinler** alanında, aşağıdaki izinleri seçin:

    - Okundu
    - Ekle
    - Oluştur
    - Yaz
    - Dil
    - Liste

14. **SAS belirteci ve URL oluştur**'u seçin.
15. **Blob SAS URL** alanındaki değeri kopyalayın ve saklayın. Bu değer sonraki yordamda kullanılacak ve *paylaşılan erişim imza URI*'si olarak anılacaktır.
16. Elektronik faturalama ile kullanmayı planladığınız anahtar kasasını açın.
17. **Ayarlar** \> **Gizli anahtarlar** ögesine gidin ve bir gizli anahtar oluşturmak için **Oluştur/içe aktar**'ı seçin.
18. **Gizli anahtar oluştur** sayfasında **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.
19. Gizli anahtarın adını girin. Bu ad, Regulatory Configuration Service (RCS) içindeki servisin kurulumu sırasında kullanılacaktır ve *anahtar kasası gizli anahtar adı* olarak anılacak. RCS kurulumu hakkında daha fazla bilgi için bkz. [Regulatory Configuration Service (RCS) kurulumu](e-invoicing-set-up-rcs.md).
20. **Değer** alanında, önceden kopyaladığınız paylaşılan erişim imzası URI'sini girin.
21. **Oluştur**'u seçin.
