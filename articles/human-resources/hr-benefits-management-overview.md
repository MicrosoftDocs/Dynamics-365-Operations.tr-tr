---
title: Kazanç yönetimine genel bakış
description: Dynamics 365 Human Resources'Deki sosyal haklar yönetimi önizleme özelliğinin Özeti. Çalışanlarınızı kullanımı kolay bir çevrimiçi deneyim sayesinde çalışanlarınızın genişletilmiş sosyal haklar seçeneklerini sunun.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029475"
---
# <a name="benefits-management-overview"></a>Kazanç yönetimine genel bakış

[!include [banner](includes/preview-feature.md)]

Rekabet edebilir durumda kalmak için, en iyi çalışanlarınızı ele almak ve bunları korumak amacıyla zengin bir avantaj kümesi sunmalısınız. Tıp ve diş kapsamı gibi standart avantajlara ek olarak, benimseme yardımı, dinlenme programları ve giyme gibi genişletilmiş hizmetler de sunmak isteyebilirsiniz. Microsoft Dynamics 365 Human Resources'un sosyal haklar yönetimi önizleme özelliği, çok çeşitli avantaj seçeneklerini destekleyen esnek bir çözüm sağlar. İnsan Kaynakları ayrıca, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi de içerir.

- Geliştirilmiş kazançlar planları, benzersiz kazanç planları oluşturmanıza ve yönetmenize ve karmaşık kazanç oranı tabloları ve iç içe geçmiş katmanları desteklebilmenizi sağlar. Daha kolay bir çalışan deneyimi için, kolayca kazanç programları, paketleri ve otomatik kayıt kuralları oluşturabilirsiniz.

- Esnek kredi programları, emeklilik ve diğer ömür olaylarını desteklemeye yönelik bir program sağlar.

- Kapsamlı uygunluk kuralları, doğru çalışanların hak kazanın uygun olmasını sağlamayacaklarından emin olmanızı sağlar.

- Çevrimiçi yararlar kaydı, çalışanlarınız için kolay bir deneyim sağlar.

- Nitelikli ömür olayı işleme, çalışan self servis ile tümleşir ve gelecekteki ömür olaylarını destekler.

Demo verilerine erişmek istiyorsanız korumalı alan ortamınızı yeniden dağıtmanız gerekir.

Doğrudan geri bildirim veya konu rapor verebilirsiniz: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Kazanç yönetimiyle ilgili bilinen sorunlar

### <a name="eligibility-processing"></a>Uygunluk işleniyor

1-5X maaş, yüzde maaş ve sabit tutar karşılama tutarı kullanan avantajlar için uygunluğu çalıştırırken , **kullanım ayrıntıları** tarihini **çalışma geçmişi** içindeki **çalışan başlangıç tarihine** ayarlamalısınız. **Çalışılan saatleri**, **ödeme sıklığını** ve **yıllık kazançlar maaş tutarını** da dahil etmelisiniz. Çalışanın sabit dengelemesi varsa, **çalışılan saatleri** ve **ödeme sıklığını** girin. Yıllık maaş tutarı hesaplanır. Çalışan maaşlı ise, **çalışılan saatleri** girmeniz gerekmez. Yeni çalışanlar oluştururken önce sabit ücret girilmesini öneririz. Avantaj ayrıntıları kaydını güncelleştirmek için, **çalışan > çalışan geçmişi > istihdam ayrıntılarına** gidin. Tarihi çalışanın başlangıç tarihine ayarlayın.

### <a name="employee-self-service"></a>Personel self servisi

Ömür için karşılama tutarı güncelleştirilirken çalışan tutarı hesaplamaz. Örneğin bir çalışana bir hayat sigortası planı sunulduğunda 1000 liralık karşılama tutarı başına 36 kuruşluk maliyetle 50.000 liraya kadar bir karşılama tutarı seçebilir.  Çalışan karşılama tutarını güncelleştirdiğinde, çalışanın ilişkili maliyeti sıfır olarak kalır.

Bu plan türünde yalnızca tek bir seçime izin veren bir kazanç planı için, bir plan seçtikten sonra bir planı feragat etmeye çalışırsa Kullanıcı bir hata alır. Örneğin kullanıcı bir tıbbi plan seçip alışveriş sepetine ekliyor. Bunun ardından, başka bir tıbbi plan için **Feragat**'i seçiyor. Kullanıcı bir hata alacaktır.

## <a name="enable-benefits-management"></a>Kazanç Yönetimni etkinleştirme

Kazançlar yönetimi bir önizleme özelliğidir ve yalnızca **korumalı alan** ortamlarında kullanılabilir. Bu makalelerde İnsan Kaynakları Önizleme özelliklerinin nasıl açılacağı açıklanır. Bunlar ayrıca, sosyal haklar yönetimini etkinleştirdiğinizde İnsan Kaynakları olan, sosyal haklar yönetiminin hangi varolan özelliklerinin yerini aldığını veya devre dışı bırakıldığını da bildirir.

- [Özellikleri yönetme](hr-admin-manage-features.md)
- [Önizleme özelliği: Kazanç yönetimi](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Kazanç yönetimini yapılandırma

Çalışanlarınız için kazanç planları oluşturabilmeniz için, planların seçeneklerini konfigüre etmeniz gerekir.

- [Kazanç yönetimi parametrelerini ayarlama](hr-benefits-setup-parameters.md)
- [Uygunluk kurallarını ve seçeneklerini yapılandırma](hr-benefits-setup-eligibility-rules.md)
- [Kişisel iletişim uygunluk seçeneklerini yapılandırma](hr-benefits-setup-contact-eligibility-options.md)
- [Kapsam seçeneklerini oluşturma](hr-benefits-setup-coverage-options.md)
- [Ödeme sıklıklarını ayarlama](hr-benefits-setup-payment-frequencies.md)
- [Yaşam olayı türlerini yapılandırma](hr-benefits-setup-life-event-types.md)
- [Plan türleri oluşturma](hr-benefits-setup-plan-types.md)
- [Neden kodlarını ayarla](hr-benefits-setup-reason-codes.md)
- [Katman kodlarını ayarlama](hr-benefits-setup-tier-codes.md)
- [Oranları yapılandırma](hr-benefits-setup-rates.md)
- [Kesintileri yapılandırma](hr-benefits-setup-deductions.md)
- [Bekleme günlerini yapılandırma](hr-benefits-setup-waiting-days.md)
- [Bekleme dönemlerini yapılandırma](hr-benefits-setup-waiting-periods.md)
- [Yuvarlama kurallarını ayarlama](hr-benefits-setup-rounding-rules.md)
- [İstihdam kategorileri oluşturma](hr-benefits-setup-employment-categories.md)
- [İstihdam türlerini ayarlama](hr-benefits-setup-employment-types.md)
- [Personel self servisini yapılandırma](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Kazanç planları oluşturma

Bu makaleler, ambalajlarla esnek kredi programları dahil olmak üzere kazanç planlarının nasıl oluşturulacağını gösterir.

- [Kazanç planlarını ayarlama](hr-benefits-plans-setup.md)
- [Çalışan kazanç planları oluşturma](hr-benefits-plans-worker.md)
- [Esnek kredi programları ayarlama](hr-benefits-plans-flex-credit-programs.md)
- [Gelecekteki yaşam olaylarını yapılandırma](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Kazanç planlarını işleme

Yaptığınız değişikliklerin bazılarını etkin hale getirmek için onları işlemeniz gerekir.

- [Kayıt uygunluğunu işleme](hr-benefits-process-enrollment-eligibility.md)
- [Yaşam olaylarını işleme](hr-benefits-process-life-events.md)
- [Yaşam olayı değişikliklerini işleme](hr-benefits-process-life-event-changes.md)
- [Yaşam olayı uygunluğunu işleme](hr-benefits-process-life-event-eligibility.md)
- [Oran değişikliklerini işleme](hr-benefits-process-rate-changes.md)

