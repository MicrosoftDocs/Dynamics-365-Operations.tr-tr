---
title: "Tüzel kişilikler arasında İK parametreleri ayarlama"
description: "Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e73441a3f4190561d1d16db40ee1581267c8dfb
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Tüzel kişilikler arasında İK parametreleri ayarlama

[!INCLUDE [banner](includes/banner.md)]

Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır.

Bazı kayıt türleri konum kayıtları gibi şirketler arasında paylaşılır. Bu kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Örneğin, **İnsan Kaynakları parametreleri paylaşılan** sayfasını tüzel kişilikler arasında İnsan Kaynakları parametreleri ayarlamak için kullanırsınız. 

**İnsan Kaynakları paylaşılan parametreleri** sayfasında, parametreler kendi işlevselliğine dayalı alanlar halinde gruplandırılır. 

### <a name="previously-released-functionality"></a>Daha önce yayımlanan işlev
**kimlik** sekmesinde sayfada listelenen kimlik numaralarını temsil eden kimlik türleri seçmelisiniz. Çalışanlar için kimlik bilgilerini girmeden önce kimlik tiplerini ayarlamanız gerekir. Sosyal Güvenlik numarası, Ulusal kimlik numarası, yabancı kimlik numarası ve kişisel kimlik kodu hakkında bilgiler **kimlik türü** sayfasında saklanır. Yeni bir kimlik türü tanımlamak veya mevcut türlerin listesini gözden geçirmek için **Personel yönetimi** &gt; **Bağlantılar sekmesi** &gt; **Kurulum** &gt; **Kimlik türleri**'ne tıklayın. Basit bir kod ve açıklama girebilirsiniz. 

### <a name="if-youre-using-dynamics-365-for-talent"></a>Dynamics 365 for Talent kullanıyorsanız
**kimlik** sekmesinde sayfada listelenen kimlik numaralarını temsil eden kimlik türleri seçmelisiniz. Çalışanlar için kimlik bilgilerini girmeden önce kimlik tiplerini ayarlamanız gerekir. Sosyal Güvenlik numarası, Ulusal kimlik numarası, yabancı kimlik numarası ve kişisel kimlik kodu hakkında bilgiler **kimlik türü** sayfasında saklanır. Yeni bir kimlik türü tanımlamak veya mevcut türlerin listesini gözden geçirmek için **İnsan Kaynakları** &gt; **Kurulum** &gt; **Kimlik türleri**'ne tıklayın. Basit bir kod ve açıklama girebilirsiniz. 

**Numara sıraları** sekmesinde, aşağıdaki kayıtlar için kullanılan numara serilerini seçebilirsiniz: Personel numarası, pozisyon, kullanıcı isteği kimliği, I-9 belgesi, başvuran, tartışma, yararı kimliği ve personel eylem (Bu kayıt türü etkinleştirilmişse). Numara serisi referanslarını ve kodlarını tanımlamak için **Numara serisi** listesi sayfasını kullanın. Bu sayfayı bulmak için sayfa arama özelliğini kullanın. 

**pozisyonlar** sekmesinde, varsayılan olarak atama için kullanılabilir olan yeni pozisyonlar olup olmadığını gösterin:

-   **Her zaman** – Pozisyonlar oluşturulurken çalışanları yeni pozisyonlara atayamazsınız. Pozisyonlar oluşturulurken, **Pozisyon** sayfasının **Genel** sekmesindeki **Atama için kullanılabilir** tarih ve saat, oluşturma tarihi ve saatine otomatik olarak ayarlanır.
-   **Hiçbir zaman** – pozisyonlar oluşturduğunuzda yeni konumlara çalışanları atayamazsınız. Bu seçeneği belirlerseniz, her yeni pozisyon için kullanılabilir duruma geldiğinde **konumu** sayfasını açmanız ve daha sonra **genel** sekmesinde, çalışan atamasını etkinleştirmek için **atama için kullanılabilir** tarihini girin.


<a name="see-also"></a>Ayrıca bkz.
--------

[Şirkete özgü İK parametreleri ayarlama](set-up-company-specific-hr-parameters.md)




