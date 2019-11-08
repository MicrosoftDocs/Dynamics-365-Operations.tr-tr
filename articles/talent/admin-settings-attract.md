---
title: Microsoft Dynamics 365 Talent  - Attract'ta şirket bilgilerini yapılandırma
description: Bu konuda, Microsoft Dynamics 365 Talent  - Attract için şirket bilgilerinin ve markasının nasıl yapılandırılacağı açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7013065a9494cb407020de2ebcad4058dd57c6c4
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551618"
---
# <a name="configure-company-information-in-microsoft-dynamics-365-talent---attract"></a>Microsoft Dynamics 365 Talent  - Attract'ta şirket bilgilerini yapılandırma
[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract Yönetim merkezinde Attract uygulaması için yapılandırma ayarları, tümleştirme seçenekleri ve ayar seçeneklerini bulunur.

## <a name="company-information"></a>Şirket bilgileri

Şirket için bir görünen ad girin ve şirket logosu ekleyin. Görünen ad ve logo, iş gönderileri ve işe alım deneyimi sırasında kullanılabilir.

## <a name="linkedin-integration"></a>LinkedIn Tümleştirmesi

LinkedIn Recruiter System Connect (RSC) ile tümleştirmeyi ayarlayın. LinkedIn kimlik bilgilerinizi kullanarak LinkedIn'e bağlandıktan sonra adayın LinkedIn profili, uygulamaları, görüşme geribildirimi ve işe alım ekibi notlarını eşitleyebilirsiniz. Tam LinkedIn işveren lisansı gereklidir. LinkedIn Recruiter hakkında daha fazla bilgi için bkz. [Recruiter System Connect (RSC) – SSS](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Kullanıcı izinleri

Kurumunuzdaki kullanıcılara roller atayın. Aşağıdaki roller kullanılabilir: **Yönetici**, **İşveren**, **İşe Alma Yöneticisi** ve **Salt okunur**. Kullanıcı izinleri hakkında daha fazla bilgi için bkz: [Attract'te güvenlik ve rol yönetimi](./security-attract.md).

## <a name="feature-management"></a>Özellik yönetimi

Yeni özellikler eklendiğinde herkese açık bir önizlemede sunulabilir. Herkese açık önizleme özellikleri tüm servis gereksinimlerini karşılamaz. Bunları alarak verilerinizi dış sistemlerle paylaşımı kabul ediyorsunuz. Kuruluşunuzun yayımlanan tüm yeni özellikleri gerektirmediğini görebilirsiniz. Kurumunuzun ihtiyaçlarına bağlı olarak herkese açık özellikleri açıp kapatabilirsiniz.

## <a name="template-management"></a>Şablon yönetimi

İşlem şablonu, bir işin işe alma işleminin parçası olarak dahil edilmesi gereken tüm faaliyetleri içerir. Kurumunuz, tüm ekip üyeleri veya yalnızca yöneticilerin işe alma işlem şablonları oluşturmasına izin verebilir. Ekip üyelerinin kendi işe alma işlem şablonlarını oluşturmasına izin vermek için Şablon yönetimi işlevini etkinleştirin. İşlem şablonları hakkında daha fazla bilgi için bkz. [Attract'ta işlem şablonları](./process-templates-attract.md).

## <a name="email-template-settings"></a>E-posta şablonu ayarları

Kuruluşlar, çeşitli senaryolar için e-posta şablonları oluşturabilir. E-posta şablonlarını dahil edecek başlık resmi seçebilirsiniz. Seçili başlık daha sonra tüm e-posta şablonları içinde görünür. Şablon altbilgisinde, kuruluşunuzun gizlilik bildirimine ve iletişim için kullanım koşullarına bir bağlantı ekleyebilirsiniz. Daha fazla bilgi için bkz. [Attract'ta e-posta şablonları](./email-templates.md).

## <a name="offer-process"></a>Teklif süreci

İş teklifleri için onay işlemi yapılandırabilirsiniz. Örneğin, bir teklifin adaya gönderilmeden önce onaylanmasının gerekli olup olmadığını belirtebilirsiniz. Onaylayanların teklifle ilgili kararlarıyla birlikte bir açıklama yapmasını gerekli kılabilirsiniz.

İki onay iş akışı kullanılabilir: **Paralel** ve **Ardışık**.

- **Paralel** – Onaylar aynı anda tüm onaylayanlara gönderilir.
- **Ardışık** – Onaylar, onaylayanlara belli bir sırayla gönderilir.

Aday deneyimiyle ilgili seçenekleri de yapılandırabilirsiniz. Örneğin, bir seçenek adayların ek tartışma olmadan bir teklifi reddedip reddedemeyeceğini belirlemenizi sağlar. **Adaylara ek tartışma olmadan bir teklifi reddetmesi izni ver** seçeneğini **Hayır** olarak ayarladıysanız **Teklifi reddet** düğmesine tüm adaylar erişebilir. Bu seçeneği **Evet** olarak ayarladıysanız adaylarbir neden ve daha sonra **Teklifi reddet**'i seçerek teklifi reddedebilir..

Teklifleri için bitiş tarihi ayarlayabilir ve uygulayabilirsiniz. **Tüm teklifleri için bitiş tarihi gerekli** seçeneğini **Evet** ayarladıysanız, belirttiğiniz gün veya saat sayısından sonra teklifler sona erer.

Teklif yönetimi hakkında daha fazla bilgi için bkz [Teklif yönetimini ayarla](./offer-setup.md).
