---
title: Kuruluş yönetimi giriş sayfası
description: Bu konuda, kuruluşunuzda kullanmanıza yardımcı olacak kaynaklar açıklanmaktadır.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b1b519d116a55c255cf90d9478ee1714de90264
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811346"
---
# <a name="organization-administration-home-page"></a>Kuruluş yönetimi giriş sayfası

[!include [banner](../includes/banner.md)]

Bu konuda kullanıcı ve yöneticilerin sistemi kuruluşunuz ve işletmeniz için sorunsuz ve etkili çalışacak şekilde yapılandırmalarına yardımcı olacak içerik sunulmaktadır.

Burada listelenen içeriğin büyük bölümü **Kuruluş yönetimi** modülündeki özelliklere uygulanır. Ancak, bir kayıt şablonu oluşturmak ve kullanmak gibi bazı görevler, kuruluşunuzun daha verimli çalışmasına yardımcı olmak için her modülde gerçekleştirilebilir.

## <a name="number-sequences"></a>Numara serileri

Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, *referans* olarak adlandırılır. Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.

- [Numara sıralarına genel bakış](number-sequence-overview.md)
- [Sihirbaz kullanarak numara sıraları ayarlama](tasks/set-up-number-sequences-wizard.md) (Görev kılavuzu)
- [Bireysel olarak numara serileri ayarlama](tasks/set-up-number-sequences-individual-basis.md) (Görev kılavuzu)

## <a name="organizations"></a>Kuruluşlar

Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.

Kuruluşları ve kuruluş hiyerarşilerini ayarlamadan önce işletmenizin nasıl modelleneceğini planladığınızdan emin olun. Kuruluş modelinin uygulama ve iş süreçleri üzerinde önemli bir etkisi vardır.

- [Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](organizations-organizational-hierarchies.md)
- [Kuruluş hiyerarşinizi planlama](plan-organizational-hierarchy.md)
- [Bir kuruluş hiyerarşisi oluşturma](tasks/create-organization-hierarchy.md) (Görev kılavuzu)
- [Tüzel kişilik oluşturma](tasks/create-legal-entity.md) (Görev kılavuzu)
- [Bir işletme birimi oluşturma](tasks/create-operating-unit.md) (Görev kılavuzu)

## <a name="address-books"></a>Adres defterleri

Genel adres defteri, şirketin etkileşimde bulunduğu tüm iç ve dış kişiler ve kuruluşların depolanması gereken verilerini barındıran merkezi bir depodur. Taraf kayıtları ile ilişkilendirilen veri, tarafın adını, adresini ve ilgili kişi bilgisini içerir.

Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz.

- [Genel adres defterine genel bakış](overview-global-address-book.md)
- [Genel adres defteri ve diğer adres defterleri için planlama](plan-configuration-global-address-book-additional-address-books.md)
- [Genel adres defterini yapılandırma](tasks/configure-global-address-book.md)
- [Adres defterleriyle ilgili SSS](qa-address-books.md)

## <a name="workflow"></a>İş akışı

İş akışı, bağımsız iş akışları veya iş süreçleri oluşturmak için kullanabileceğiniz bir sistemdir. Bir iş akışı oluşturduğunuzda, bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlarsınız.

- [İş akışı sistemine genel bakış](overview-workflow-system.md)
- [İş akışı öğeleri](workflow-elements.md)
- [İş akışı onay süreçlerindeki eylemler](workflow-actions.md)
- [İş akışlarına genel bakış](create-workflow.md)

## <a name="electronic-signatures"></a>Elektronik imzalar

Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular. Bazı sektörlerde, elektronik imza yasal açıdan elle atılmış imza kadar bağlayıcı olmaktadır. Elektronik imzalar ilaç, yiyecek ile içecek ve havacılık ve uzay ile savunma sanayileri gibi birtakım kontrol altındaki sektörlerle ilgili yönetmeliklere uyumluluk gereklilikleridir.

Önemli iş süreçleri için elektronik imza kullanabilirsiniz. Bazı işlemler yerleşik elektronik imza özelliklerine sahiptir. Ayrıca herhangi bir veritabanı tablosu ve alanı için özel imza gereklilikleri de oluşturabilirsiniz.

- [Elektronik imzalara genel bakış](electronic-signature-overview.md)
- [Elektronik imzaları ayarlama](tasks/set-up-electronic-signatures.md) (Görev kılavuzu)

## <a name="case-management"></a>Servis talebi yönetimi

Planlayarak, izleyerek ve durumları analiz ederek, benzer sorunlarda kullanılabilecek verimli çözümler geliştirebilirsiniz. Örneğin, bir müşteri servis temsilcisi veya İnsan Kaynakları kişisi vakalar oluşturduğunda, bir vaka ile çalışma veya bunu çözümlemek için yardımcı olabilecek bilgileri bilgi bankası makalelerinde bulabilirler.

- [Servis talebi yönetimine genel bakış](cases.md)
- [Servis talebi kategorisi güvenliğini, servis talebi işlemlerini ve servis talebi kategorilerini planlama](plan-case-management.md)

## <a name="record-templates"></a>Kayıt şablonları

Kayıt şablonları, kayıtları daha hızlı oluşturmaya yardımcı olabilir. Sıklıkla kullanılan alan değerlerinin her yeni bir kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunu oluşturabilirsiniz.

- [Kayıt şablonlarına genel bakış](record-templates.md)
- [Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Görev kılavuzu)
- [Yeni kayıt oluşturmak için kayıt şablonu kullanma](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Görev kılavuzu)

## <a name="general-organization-administration"></a>Genel kuruluş yönetimi

- [Başlık resmi veya logoyu değiştirme](../get-started/tasks/change-banner-or-logo.md) (Görev kılavuzu)
- [Belge yönetimini konfigüre etme](configure-document-management.md)
- [E-postayı yapılandırma ve gönderme](configure-email.md)
- [Tarih/saat tarih ve saat dilimleri](date-time-zones.md)
