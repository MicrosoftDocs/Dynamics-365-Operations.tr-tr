---
title: Kazanç yönetimine genel bakış
description: Bu konuda, Dynamics 365 Human Resources uygulamasındaki Kazanç yönetimi özelliğine genel bir bakış sağlanmaktadır.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 696c7632fd8adda71b2b67d59fba7f7d83193f5b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065955"
---
# <a name="benefits-management-overview"></a>Kazanç yönetimine genel bakış


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rekabet edebilir durumda kalmak için, en iyi çalışanlarınızı ele almak ve bunları korumak amacıyla zengin bir avantaj kümesi sunmalısınız. Tıp ve diş kapsamı gibi standart avantajlara ek olarak, benimseme yardımı, dinlenme programları ve giyme gibi genişletilmiş hizmetler de sunmak isteyebilirsiniz. Microsoft Dynamics 365 Human Resources uygulamasında kazanç yönetimi, çok çeşitli kazanç seçeneklerini destekleyen esnek bir çözüm sağlar. İnsan Kaynakları ayrıca, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi de içerir.

- Geliştirilmiş kazançlar planları, benzersiz kazanç planları oluşturmanıza ve yönetmenize ve karmaşık kazanç oranı tabloları ve iç içe geçmiş katmanları desteklebilmenizi sağlar. Daha kolay bir çalışan deneyimi için, kolayca kazanç programları, paketleri ve otomatik kayıt kuralları oluşturabilirsiniz.
- Esnek kredi programları, emeklilik ve diğer ömür olaylarını desteklemeye yönelik bir program sağlar.
- Kapsamlı uygunluk kuralları, doğru çalışanların hak kazanın uygun olmasını sağlamayacaklarından emin olmanızı sağlar.
- Çevrimiçi yararlar kaydı, çalışanlarınız için kolay bir deneyim sağlar.
- Uygun yaşam olayı işleme işlemi gelecekteki yaşam olaylarını destekler.

Demo verilerine erişmek istiyorsanız korumalı alan ortamınızı yeniden dağıtmanız gerekir.

> [!NOTE]
> Artık Kazançlar yönetimi sayfalarını özelleştirebilirsiniz. Kazanç planları için **Kapsam seçeneği** sayfasına kapsam oranları ile ilgili özel alanlar eklenebilir. Özel alanlarla çalışma hakkında daha fazla bilgi için bkz. [Özel alanlar](hr-developer-custom-fields.md).
>
> ![Kazançlar yönetimi özel alanları](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Kazanç Yönetimni etkinleştirme

Bu konuda, Human Resources'taki özelliklerin nasıl etkinleştirileceği açıklanmaktadır. Ayrıca Human Resources'taki mevcut özelliklerin hangilerinin Kazanç yönetimiyle değiştirildiği ve Kazanç yönetimini etkinleştirdikten sonra hangi özelliklerin devre dışı bırakıldığı da açıklanmaktadır.

> [!IMPORTANT]
> **Üretim** ortamında Kazanç yönetimini etkinleştirdikten sonra devre dışı bırakamazsınız. **Üretim** ortamında etkinleştirmeden önce Kazanç yönetimini **Korumalı alan** ortamında etkinleştirmenizi ve test etmenizi öneririz. Eski Kazanç işlevi ile ek kurulum gerektiren yeni Kazanç yönetimi işlevi arasında önemli farklar vardır ve üretim ortamına alınmadan önce test edilmesi gerekir.

Daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

## <a name="process-overview"></a>İşleme genel bakış

Yan hakları yapılandırma işlemi aşağıdaki görevleri içerir:

1.  Gerekli yan hak bilgilerini ayarlama.
2.  İsteğe bağlı yan hak bilgilerini ayarlama.
3.  Yan hak planlarını ayarlama.
4.  Esnek kredi programları ayarlama (isteğe bağlı).
5.  Gerekli personel bilgilerini yapılandırma.
6.  İsteğe bağlı personel bilgilerini yapılandırma.
7.  Uygunluğu belirlemek için çalışanları işleme.
8.  Çalışanlar, Çalışan Self Servisi hizmeti aracılığıyla planları seçer (isteğe bağlı).
9.  Çalışan planı seçimlerini onaylama.
10. Yaşam olayı işleme (isteğe bağlı).
11. Ücret güncellemeleri (isteğe bağlı).

## <a name="set-up-required-benefit-information"></a>Gerekli yan hak bilgilerini ayarlama

Çalışanların planlara kaydedilebilmesi için önce birden çok bileşen ayarlanmalıdır:

- **Yan hak yönetimi parametreleri**: Bu ayarlar şirketler arasında paylaşılır. Varsayılan neden kodlarını ayarlayabilir, **Yan hak yıllık maaş** seçeneğini etkinleştirebilir, yeni işe alınanlar için varsayılan bir ödeme sıklığı ayarlayabilir ve yaşam olaylarını etkinleştirebilirsiniz. Daha fazla bilgi için bkz. [Yan hak yönetimi parametrelerini ayarlama](hr-benefits-setup-parameters.md).
- **Kişisel ilgili kişi uygunluk seçenekleri**: Kişisel ilgili kişiler, belirlenen planlarda bakılmakla yükümlü kişiler veya yararlanacak kişilerdir. Genellikle, çocuklar, eşler veya sorumlulardır. Daha fazla bilgi için bkz. [Kişisel iletişim uygunluk seçeneklerini yapılandırma](hr-benefits-setup-contact-eligibility-options.md).
- **Kapsam seçenekleri**: Bir plan için kullanılabilir olacak kapsam türlerini ayarlayın. Özellikle, kimlerin kapsama alınması gerektiğini veya ne kadar kapsama alanı olduğunu tanımlayın. Daha fazla bilgi için bkz. [Kapsam seçeneklerini oluşturma](hr-benefits-setup-coverage-options.md).
- **Plan türleri**: Bir yan hak planı oluşturduğunuzda kullanılabilecek plan türlerini ayarlayın. Örnek plan türleri **Diş**, **Göz** ve **Birikim** verilebilir. Plan türündeki bazı önemli ayarlar, yan hak planında kullanılabilen ayarları belirler. Daha fazla bilgi için, bkz. [Plan türleri oluşturma](hr-benefits-setup-plan-types.md).
- **Uygunluk kuralları**: Uygunluk kuralları, bir çalışanın bir plan için uygun olup olmadığını belirlemek için kullanılır. Her yan hak planıyla en az bir uygunluk kuralı ilişkilendirilmelidir. Daha fazla bilgi için bkz. [Uygunluk kurallarını ve seçeneklerini yapılandırma](hr-benefits-setup-eligibility-rules.md).
- **Ödeme sıklıkları**: Yan hak ücretleri yapılandırıldığında ödeme sıklıkları gereklidir. Bir ücret için kullanılan ödeme sıklığı, personel ve/veya işverenin haftalık, aylık veya yıllık olarak borçlu olduğu tutarı belirlemeye yardımcı olur. Daha fazla bilgi için bkz. [Ödeme sıklıklarını ayarlama](hr-benefits-setup-payment-frequencies.md).
- **Ücretler**: Ücretler, bir yan hakkın çalışan veya işverene ne kadara mal olacağını tanımlar. Paranın tekrar personele tahsis edilmesi gerekiyorsa (örneğin, spor salonu üyeliğine yönelik bir kredi), negatif ücret girilir. Daha fazla bilgi için bkz. [Ücretleri yapılandırma](hr-benefits-setup-rates.md).
- **Katman oranları**: Bir ücretin bazı ölçütlere göre değişmesi gerektiğinde katman oranları kullanılır. En yaygın katman oranı, yaşa göre tek bir katmandır. Ancak, ücretin cinsiyete, yaşa veya diğer ölçütlere göre değişebileceği çift katmanlı oranlar da ayarlanabilir.
- **Kesintiler**: Kesintiler temel olarak, yan hak için kesintiyi tanımlamak için bordro sistemine aktarılacak başlık bilgileri/kodlarıdır. Bu kesintileri ayarlamalısınız çünkü yan hak planında gerekli olacaktır. Daha fazla bilgi için bkz. [Kesintileri yapılandırma](hr-benefits-setup-deductions.md).
- **Yan hak dönemleri**: Yan hak dönemi, çalışanların yan hak kapsamına sahip olacağı dönemdir. Aynı zamanda bir plan yılı olarak da bilinir. Açık kayıt dönemleri de burada ayarlanır.

## <a name="set-up-optional-benefit-information"></a>İsteğe bağlı yan hak bilgilerini ayarlama

Bir yan hak planı oluşturmak için aşağıdaki bileşenler ayarlanmalıdır:

- **Programlar**: Program, aynı uygunluk kuralları tarafından yönetilen bir dizi yan haktır. Örneğin, satış departmanındaki herkes bir cep telefonu alabilir.
- **Paketler**: Paket, ek planlar seçme seçeneği sunulmadan önce bir planın seçilmesini gerekli kılan bir yan hak grubudur. Örneğin, yüksek oranda düşülebilir bir tıbbi plan bir sağlık birikim hesabı (HSA) planıyla birlikte sunulabilir.
- **Yaşam olayı türleri**: Yaşam olayları, bir çalışanın kapsamında değişiklik olmasına izin veren olaylardır. Yaşam olayı türleri bir plan türüne bağlıdır. Örneğin, bir tıbbi plan türü, bir doğum veya evlat edinme nedeniyle veya medeni durumdaki bir değişiklik nedeniyle planlarda değişikliklere izin verebilir. Ancak, bir sigorta planı türü, yaşam olayları nedeniyle herhangi bir değişikliğe izin vermeyebilir. Daha fazla bilgi için bkz. [Yaşam olayı türlerini yapılandırma](hr-benefits-setup-life-event-types.md).
- **Bekleme günleri ve bekleme dönemleri**: Bir yan hak planında bir kapsam bekleme süresi ayarlanabilir. Örneğin, yeni işe alınan bir çalışan ancak üç aylık bir çalışmadan sonra 401(k) planına kaydolabilir. Bu durumda bekleme süresi üç aydır. Yeni kayıtlar işlenebilir ve sağlayıcıya yalnızca ayın belirli bir gününde gönderilebilirse bekleme günleri bekleme süresinde kullanılır. Örneğin, 401(k) planı kaydı sadece ayın on beşinde işlenebiliyorsa üç aylık istihdamdan sonra, belirlenen bekleme süresi üç aydır ve bekleme günü ayın on beşidir. Daha fazla bilgi için bkz. [Bekleme günlerini yapılandırma](hr-benefits-setup-waiting-days.md) ve [Bekleme dönemlerini yapılandırma](hr-benefits-setup-waiting-periods.md).
- **Neden kodları**: Neden kodları, bir çalışanın yan hakkının neden değiştiğini açıklamak için kullanılır. Daha fazla bilgi için bkz. [Neden kodlarını ayarlama](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Kazanç planlarını ayarlama

Bir yan hak planı ayarlarken, çalışanların kaydedilebilmesi için aşağıdaki adımları tamamlamanız gerekir:

- Bir yan hak dönemi atayın.
- Kapsam seçenekleri ekleyin.
- **Genel** sekmesinde geçerlilik başlangıç ve bitiş tarihi ayarlayın.
- En az bir uygunluk kuralı atayın.
- **Kurulum** sekmesinde **Kayda izin ver/devam et** alanını ayarlayın.

Yan hak planlarını ayarlama hakkında daha fazla bilgi için bkz. [Yan hak planlarını ayarlama](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Esnek kredi programları ayarlama (isteğe bağlı)

Çalışanları, önceden belirlenmiş esnek kredi sayısına göre sosyal haklar kaydetmek için, esnek kredi programlarını kullanabilirsiniz. Çalışanlar esnek kredilerinin nasıl tahsis edileceğini seçebilir. Örneğin, çalışanlar zaten eşinin sağlık sigortası planı kapsamındaysa kredilerini sağlık sigortası için kullanmak zorunda değildir. Bu nedenle, bunun yerine başka yan haklar için kullanmak isteyebilirler. Esnek kredi programları hakkında daha fazla bilgi için bkz. [Esnek kredi programları ayarlama](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Gerekli personel bilgilerini yapılandırma

Çalışanları yan haklara kaydedebilmek için gerekli bilgileri sağlamanız gerekir. 

Çalışanın kendisine atanmış bir **Pozisyonu** olmalıdır. Bir **Pozisyon**, **Çalışan ataması** güncelleştirilerek **Çalışan** veya **Pozisyon** sayfalarında çalışana atanabilir. 

Daha sonra, çalışanların başlangıç tarihinde sabit bir ücret planına kaydolmaları veya **Yıllık yan haklar maaşı** tutarına sahip olmaları gerekir. Bir çalışana **Sabit ücret** atamadan önce bir **Pozisyon** atanmalıdır. 

> [!NOTE] 
> **Sabit ücret başlangıç tarihi**, **Pozisyon atama tarihinden** önce olamaz.

Alternatif olarak, komisyonlar gibi ek ücret alan personeliniz varsa, çalışan kaydından bir **Kazançlar yıllık maaş** tutarı ekleyebilirsiniz. İnsan Kaynakları, karşılama tutarlarını belirlerken **Yıllık sabit ücret tutarı** yerine **Kazançlar yıllık maaş** alanını kullanacaktır. **Yan hak yıllık maaşı** personel işe başlama tarihi veya kazanç dönemi başlangıcı (hangisi sonraysa) itibarıyla geçerli olacaktır. Ancak, **Yan haklar yıllık maaşı**'nı atamak için bir pozisyon gerekli değildir. **Yan haklar yıllık maaşı** özelliğini etkinleştirmek için **Yan haklar yönetimi** sekmesindeki **İnsan kaynakları paylaşılan parametreleri** sayfasına gidin. Bu özellik, varsayılan olarak kapalıdır.

> [!IMPORTANT]
> Bir personel için hem **Sabit ücret** hem de **Kazançlar yıllık maaş tutarı** kaydedilirse, karşılama tutarlarını belirlemede **Kazançlar yıllık maaş** kullanılır. **Çalışan** sayfasının **İstihdam ayrıntıları** bölümünde, **Yan hak ödeme sıklığı** alanında bir değer seçmeniz gerekir.

## <a name="configure-optional-employee-information"></a>İsteğe bağlı personel bilgilerini yapılandırma
Cinsiyet veya yaşa dayalı oranlar kullanan bir kazanç planı oluşturduğunuzda, bir çalışanın kazanç maliyetini hesaplamak için doğum tarihi ve cinsiyet girmeniz gerekir.

## <a name="process-employees-to-determine-eligibility"></a>Uygunluğu belirlemek için çalışanları işleme
Çalışanlar planlara kaydedilmeden önce hangi planlara uygun olduklarını belirlemek için uygunluk işlemesi çalıştırılır. Uygunluk işleminin sonuçlarını **İşlem sonuçları görüntüleyicisi**'nde görüntüleyebilirsiniz. Daha fazla bilgi için bkz. [Kayıt uygunluğunu işleme](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Çalışanlar, **Employee Self-Service**'i kullanarak planları seçer (isteğe bağlı)

Açık kayıt gerçekleştiğinde, çalışanlar yeni işe alındığında veya bir yaşam olayı oluştuğunda, çalışanlar **Employee Self-Service**'i kullanarak yan haklarını seçebilir veya güncelleştirebilir. Daha fazla bilgi için bkz. [Çalışan Self Servisi yapılandırma](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Çalışan planı seçimlerini onaylama

Çalışanların seçtikleri yan haklar, çalışanların kendilerine kayıtlı olarak kabul edilmesi için önce onaylanmalıdır. Yan haklar çalışan adına da seçilebilir. Yan hakları seçmek veya onaylamak için **Personel** sayfasında, **Yan haklar** sekmesinde **Çalışan yan hak planları**'nı seçin. Birden fazla çalışanın yan haklarını seçmek veya onaylamak için **Çalışan yan hak planlarını toplu güncelleştirme** sayfasını kullanın.

## <a name="life-event-processing-optional"></a>Yaşam olayı işleme (isteğe bağlı)

Çalışan yaşam döngüsü sırasında, her çalışan evlilik, istihdam değişiklikleri veya bakmakla yükümlü olduğu kişiler veya yararlananlarla ilgili değişiklikler gibi çeşitli yaşam olayları yaşayabilir. Yaşam olaylarını kullanmak için bunları **Paylaşılan insan kaynakları parametreleri** sayfasında etkinleştirmeniz gerekir. Plan türleri için yaşam olayı türlerini ve yaşam olayı seçeneklerini ayarlayın.

Yaşam olaylarını işleyebilmeniz için işe alma zaman dilimi sırasında açık kaydı en az bir kere çalıştırmanız gerekir. Amerika Birleşik Devletleri'nde, açık kayıt genellikle yılda bir kez gerçekleşir. Amerika Birleşik Devletleri dışında, açık kayıt işe alma sırasında çalıştırılabilir. Yaşam olayı işleme, çalışanların bir yan hak planı seçmesini gerektirmez. Ancak, çalışanların açık kayıt işlemlerine dahil edilmiş olması gerekir. Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

- [Yaşam olaylarını işleme](hr-benefits-process-life-events.md)
- [Yaşam olayı değişikliklerini işleme](hr-benefits-process-life-event-changes.md)
- [Yaşam olayı uygunluğunu işleme](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Ücret güncelleştirmeleri (isteğe bağlı)

Bazen, bir yan hakkın ücreti plan döneminde değişir. Plana zaten kayıtlı olan çalışanların ücretlerini güncelleştirmek için ücret değişikliklerini işlemeniz gerekir. Daha fazla bilgi için bkz. [Ücret değişikliklerini işleme](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
