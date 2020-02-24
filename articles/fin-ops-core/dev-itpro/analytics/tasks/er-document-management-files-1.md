---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82b1719990caeb1b383ab806a3e09a4c4a6e41a
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026146"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan yapılandırma listesine erişim alma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * 'Litware, Inc.' sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.  
2. Litware, Inc. seçin. sağlayıcısını seçin.
3. Depolar'a tıklayın.
    * "Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.  
4. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
5. Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.
6. Havuz oluştur'a tıklayın.
7. Tamam'a tıklayın.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan müşteri fatura modeli yapılandırmasını alma
1. Filtreleri göster'e tıklayın.
2. Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "Operasyon kaynakları" için bir filtre değeri girin; "ile başlar" filtre işlecini kullanarak "Açıklama" alanında "" için bir filtre değeri girin
3. Filtreleri göster'e tıklayın.
4. Aç'a tıklayın.
5. Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.
    * İçe aktarmak için "Müşteri fatura modeli" model yapılandırmasını seçin.  
6. İçe aktar'ı tıklatın.
    * Seçili yapılandırmanın 1 sürümü için İthalat'a tıklayın.  
7. Evet'i tıklatın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. Raporlama konfigürasyonları'na tıklayın.
11. Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Belge Yönetimi dosyalarına erişimi desteklemek için türetilmiş model oluşturun.
Müşteri fatura modelinin kendinize özel yapılandırmasını Microsoft tarafından sağlanan yapılandırmadan türeterek yapılandırırsınız. Belge Yönetimi dosyalarına erişmek ve bu modeli temel alarak oluşturacağınız elektronik belgeler için kullanılabilir duruma getirmek için bu yapılandırmayı kullanırsınız.  
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
2. Yeni alana "İsimden Türet: Müşteri fatura modeli, Microsoft" yazın.
3. Ad alanına "Müşteri fatura modeli (özel)" yazın.
    * Müşteri faturası modeli (özel)  
4. Konfigürasyon oluştur'u tıklatın.

