---
title: Kazanç yönetimine genel bakış
description: Dynamics 365 Human Resources'taki Kazanç yönetimi özelliğine genel bakış. Çalışanlarınızı kullanımı kolay bir çevrimiçi deneyim sayesinde çalışanlarınızın genişletilmiş sosyal haklar seçeneklerini sunun.
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f3a5583400b21aa11e88ba48b67e56fdbb05c3f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353650"
---
# <a name="benefits-management-overview"></a>Kazanç yönetimine genel bakış

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rekabet edebilir durumda kalmak için, en iyi çalışanlarınızı ele almak ve bunları korumak amacıyla zengin bir avantaj kümesi sunmalısınız. Tıp ve diş kapsamı gibi standart avantajlara ek olarak, benimseme yardımı, dinlenme programları ve giyme gibi genişletilmiş hizmetler de sunmak isteyebilirsiniz. Microsoft Dynamics 365 Human Resources'taki Kazanç yönetimi, çok çeşitli kazanç seçeneklerini destekleyen esnek bir çözüm sağlar. İnsan Kaynakları ayrıca, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi de içerir.

- Geliştirilmiş kazançlar planları, benzersiz kazanç planları oluşturmanıza ve yönetmenize ve karmaşık kazanç oranı tabloları ve iç içe geçmiş katmanları desteklebilmenizi sağlar. Daha kolay bir çalışan deneyimi için, kolayca kazanç programları, paketleri ve otomatik kayıt kuralları oluşturabilirsiniz.

- Esnek kredi programları, emeklilik ve diğer ömür olaylarını desteklemeye yönelik bir program sağlar.

- Kapsamlı uygunluk kuralları, doğru çalışanların hak kazanın uygun olmasını sağlamayacaklarından emin olmanızı sağlar.

- Çevrimiçi yararlar kaydı, çalışanlarınız için kolay bir deneyim sağlar.

- Uygun yaşam olayı işleme işlemi gelecekteki yaşam olaylarını destekler.

Demo verilerine erişmek istiyorsanız korumalı alan ortamınızı yeniden dağıtmanız gerekir.

>[!NOTE]
>Artık Kazançlar yönetimi formlarını özelleştirebilirsiniz. Artık, kazanç planları için **Kapsama seçeneği**'ne kapsama oranlarıyla ilgili özel alanlar ekleyebilirsiniz. Özel alanlarla çalışma hakkında daha fazla bilgi için bkz. [Özel alanlar](hr-developer-custom-fields.md).
>![Kazançlar yönetimi özel alanları.](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Kazanç Yönetimni etkinleştirme

Bu konuda Human Resources'taki özelliklerin nasıl etkinleştirileceği açıklanır. Ayrıca, Kazanç yönetimini etkinleştirdiğinizde, Kazanç yönetiminin Human Resources'taki hangi mevcut özelliklerin yerini aldığını veya devre dışı bırakıldığını da bildirir.

> [!IMPORTANT]
> **Üretim** ortamında Kazanç yönetimini etkinleştirdikten sonra devre dışı bırakamazsınız. **Üretim** ortamında etkinleştirmeden önce Kazanç yönetimini **Korumalı alan** ortamında etkinleştirmenizi ve test etmenizi öneririz. Eski Kazanç işlevi ile ek kurulum gerektiren yeni Kazanç yönetimi işlevi arasında önemli farklar vardır ve üretim ortamına alınmadan önce test edilmesi gerekir.

- [Özellikleri yönetme](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Personel bilgilerini yapılandırma

Çalışanları kazançalara kaydedebilmek için gerekli bilgileri sağlamanız gerekir. Bir çalışanı başlama tarihinde bir **Sabit ücret planına** kaydetmeniz ve **Çalışan** formundaki **İstihdam ayrıntıları** bölümünde bir **Kazanç ödeme sıklığı** seçmeniz gerekir.

Komisyonlar gibi ek ücret alan personeliniz varsa, çalışan kaydından bir **Kazançlar yıllık maaş** tutarı ekleyebilirsiniz. İnsan Kaynakları, karşılama tutarlarını belirlerken yıllık sabit ücret tutarı yerine **Kazançlar yıllık maaş** alanını kullanacaktır. **Kazançlar yıllık maaş** personel işe başlama tarihi veya kazanç dönemi başlangıcı (hangisi sonraysa) itibarıyla geçerli olacaktır. Bir personel için hem sabit ücret hem de kazançlar yıllık maaş tutarı kaydedilirse, karşılama tutarlarını belirlemede kazançlar yıllık maaş kullanılır.

Cinsiyet veya yaşa dayalı oranlar kullanan bir kazanç planı oluşturduğunuzda, bir çalışanın kazanç maliyetini hesaplamak için doğum tarihi ve cinsiyet girmeniz gerekir.

## <a name="configure-benefits-management"></a>Kazanç yönetimini yapılandırma

Çalışanlarınız için kazanç planları oluşturabilmeniz için, planların seçeneklerini konfigüre etmeniz gerekir.

- [Kazanç yönetimi parametrelerini ayarlama](hr-benefits-setup-parameters.md)
- [Uygunluk kurallarını ve seçeneklerini yapılandırma](hr-benefits-setup-eligibility-rules.md)
- [Kişisel iletişim uygunluk seçeneklerini yapılandırma](hr-benefits-setup-contact-eligibility-options.md)
- [Kapsam seçeneklerini oluşturma](hr-benefits-setup-coverage-options.md)
- [Ödeme sıklıklarını ayarlama](hr-benefits-setup-payment-frequencies.md)
- [Yaşam olayı türlerini yapılandırma](hr-benefits-setup-life-event-types.md)
- [Plan türleri oluşturma](hr-benefits-setup-plan-types.md)
- [Neden kodlarını ayarlama](hr-benefits-setup-reason-codes.md)
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
- [Esnek kredi programları ayarlama](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Kazanç planlarını işleme

Yaptığınız değişikliklerin bazılarını etkin hale getirmek için onları işlemeniz gerekir.

- [Kayıt uygunluğunu işleme](hr-benefits-process-enrollment-eligibility.md)
- [Yaşam olaylarını işleme](hr-benefits-process-life-events.md)
- [Yaşam olayı değişikliklerini işleme](hr-benefits-process-life-event-changes.md)
- [Yaşam olayı uygunluğunu işleme](hr-benefits-process-life-event-eligibility.md)
- [Oran değişikliklerini işleme](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]