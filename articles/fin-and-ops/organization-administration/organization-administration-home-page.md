---
title: "Kuruluş yönetimi giriş sayfası"
description: "Bu konu sizi Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'u kuruluşunuzda kullanmanıza yardımcı olacak kaynaklara yönlendirir."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f1cff2388b02ff6dfd52a39b7f3ea90f10807096
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="organization-administration-home-page"></a>Kuruluş yönetimi giriş sayfası

[!include[banner](../includes/banner.md)]


Bu konu yetkili kullanıcıların ve yöneticilerin Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'u yapılandırmasına yardımcı olacak içeriklere yönlendirir. Bu içerik onlara sistemi kuruluşunuz ve işiniz için sorunsuz ve etkili çalışmak üzere yapılandırmalarına yardımcı olacaktır.

Burada listelenen içeriğin büyük bölümü **Kuruluş yönetimi** modülündeki özelliklere uygulanır. Ancak, bir kayıt şablonu oluşturmak ve kullanmak gibi bazı görevler, kuruluşunuzun daha verimli çalışmasına yardımcı olmak için her modülde gerçekleştirilebilir. 

<a name="number-sequences"></a>Numara serileri
----------------
Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, *referans* olarak adlandırılır. Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.

-   [Numara serilerine genel bakış](number-sequence-overview.md)
-   [Bir sihirbaz kullanarak satınalma için numara serilerini ayarlama](tasks/set-up-number-sequences-wizard.md) (Görev kılavuzu)
-   [Bireysel olarak numara serileri ayarlama](tasks/set-up-number-sequences-individual-basis.md) (Görev kılavuzu)

## <a name="organizations"></a>Kuruluşlar
Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.

Finance and Operations'da kuruluşlar ve kuruluş hiyerarşilerini ayarlamadan önce işinizin nasıl modellendirileceğini planladığınızdan emin olun. Kuruluş modelinin Finance and Operations'ın uygulanması ve iş süreçleri üzerinde önemli bir etkisi vardır.

-   [Kuruluşlar ve kuruluş hiyerarşileri](organizations-organizational-hierarchies.md)
-   [Kuruluş hiyerarşinizi planlama](plan-organizational-hierarchy.md)
-   [Bir kuruluş hiyerarşisi oluşturma](tasks/create-organization-hierarchy.md) (Görev kılavuzu)
-   [Tüzel kişilik oluşturma](tasks/create-legal-entity.md) (Görev kılavuzu)
-   [Bir işletme birimi oluşturma](tasks/create-operating-unit.md) (Görev kılavuzu)

## <a name="address-books"></a>Adres defterleri
Genel adres defteri, şirketin etkileşimde bulunduğu tüm iç ve dış kişiler ve kuruluşların depolanması gereken verilerini barındıran merkezi bir depodur. Taraf kayıtları ile ilişkilendirilen veri, tarafın adını, adresini ve ilgili kişi bilgisini içerir. 

Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz. 

-   [Genel adres defteri](overview-global-address-book.md)
-   [Genel adres defteri ve diğer adres defterlerini yapılandırmayı planlama](plan-configuration-global-address-book-additional-address-books.md)
- [Genel adres defterini yapılandırma](tasks/configure-global-address-book.md)
-   [Adres defterleriyle ilgili SSS](qa-address-books.md)


## <a name="workflow"></a>İş akışı
İş akışı, Finance and Operations ile yüklenen ve tek iş akışları veya iş süreçleri oluşturmakta kullanabileceğiniz bir sistemdir. Bir iş akışı oluşturduğunuzda, bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlarsınız. 

-   [İş akışı özeti](overview-workflow-system.md)
-   [İş akışı öğeleri](workflow-elements.md)
-   [İş akışı eylemleri](workflow-actions.md)
-   [İş akışı oluşturma](create-workflow.md)

## <a name="electronic-signatures"></a>Elektronik imzalar
Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular. Bazı sektörlerde, elektronik imza yasal açıdan elle atılmış imza kadar bağlayıcı olmaktadır. Elektronik imzalar ilaç, yiyecek ile içecek ve havacılık ve uzay ile savunma sanayileri gibi birtakım kontrol altındaki sektörlerle ilgili yönetmeliklere uyumluluk gereklilikleridir.

Finance and Operations uygulamasında önemli iş süreçleri için elektronik imza kullanabilirsiniz. Bazı işlemler yerleşik elektronik imza özelliklerine sahiptir. Ayrıca herhangi bir veritabanı tablosu ve alanı için özel imza gereklilikleri de oluşturabilirsiniz.

-   [Elektronik imzalara genel bakış](electronic-signature-overview.md)
-   [Elektronik imzaları ayarlama](tasks/set-up-electronic-signatures.md) (Görev kılavuzu)

## <a name="case-management"></a>Servis talebi yönetimi
Planlayarak, izleyerek ve durumları analiz ederek, benzer sorunlarda kullanılabilecek verimli çözümler geliştirebilirsiniz. Örneğin, bir müşteri servis temsilcisi veya İnsan Kaynakları kişisi vakalar oluşturduğunda, bir vaka ile çalışma veya bunu çözümlemek için yardımcı olabilecek bilgileri bilgi bankası makalelerinde bulabilirler. 

-   [Servis talebi yönetimine genel bakış](cases.md)
-   [Servis talebi güvenliğini, işlemlerini ve kategorilerini yapılandırma](plan-case-management.md)

## <a name="record-templates"></a>Kayıt şablonları
Kayıt şablonları, kayıtları daha hızlı oluşturmaya yardımcı olabilir. Sıklıkla kullanılan alan değerlerinin her yeni bir kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunu oluşturabilirsiniz. 

-   [Kayıt şablonları](record-templates.md)
- [Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Görev kılavuzu)
- [Yeni kayıt oluşturmak için kayıt şablonu kullanma](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Görev kılavuzu)

## <a name="general-organization-administration"></a>Genel kuruluş yönetimi
-   [Başlık resmi veya logoyu değiştirme](../get-started/tasks/change-banner-or-logo.md) (Görev kılavuzu)
- [Belge yönetimini konfigüre etme](configure-document-management.md)
- [E-postayı yapılandırma ve gönderme](configure-email.md)
-   [Tarih/saat tarih ve saat dilimleri](date-time-zones.md)








