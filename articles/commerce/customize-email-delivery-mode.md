---
title: Teslimat şekline göre işlem tabanlı e-postaları özelleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce'ta belirli bildirim türleri ve teslimat modları için özel e-posta şablonları ayarlamayı açıklamaktadır .
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: faf5fba70bf9297727464e6046806696ab725001
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595005"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Teslimat şekline göre işlem tabanlı e-postaları özelleştirme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta belirli bildirim türleri ve teslimat modları için özel e-posta şablonları ayarlamayı açıklamaktadır .

İşlem e-postaları artık bildirim türü (örneğin, **sipariş oluşturuldu**, **sipariş edilen sipariş** veya **fatura kesilen sipariş**) ve teslimat modu (örneğin, fazla gece, mağaza içi teslim veya yol kenarı teslim) birleşimi için özelleştirilebilir. Özel işlem e-postaları perakendecilerin, siparişin teslimat moduna göre tasarlanmış olan karşılama deneyimleriyle ilgili olarak müşterilerine sipariş vermalarını sağlar. Örneğin, "sipariş edilen" olayı özelleştirilebilir bir yan malzeme çekme seçimi yapan müşteriler için yol kenarı teslim yönergeleri sağlar. Alternatif olarak, siparişleri sevk edilmesini seçen müşteriler için sevkiyat taşıyıcısı ve teslimat bilgileri sağlayabilir.

> [!NOTE]
> Özelleştirilmiş işlem e-postalarında işlevselliği kullanmak için, önce Commerce Headquarters'da **çalışma alanları \> Özellik Yönetimi**'ne giderek işlem e-posta şablonlarını, **teslimat moduna göre Özelleştir** seçeneğini etkinleştirmeniz gerekir .

E-postalar aşağıdaki bildirim türleri için teslimat modu ile özelleştirilebilir.

- **Sipariş iptali** – Bu e-posta bildirim türü yenidir.
- **Sipariş oluşturuldu**
- **Sipariş onaylandı**
- **Sipariş faturası kesildi** – Bu e-posta bildirim türü yenidir. Sevk emri teslim modu (malzeme çekme, gerçekleştirme veya elektronik teslimat modu değil) olan herhangi bir fatura olayı için bildirim gönderecek bir **sipariş sevk** bildirim türü yerine kullanılabilir.
- **Çekilen sipariş**
- **paketlenmiş sipariş**
- **Sipariş alma için hazır** – Bu bildirim türü yalnızca **Çoklu malzeme çekme dağıtım modları desteği** etkinse teslimat modu ile özelleştirilebilir. Bu durumda, bu bildirim türü işlevsel olarak **sipariş edilen** bildirim türüne eşdeğerdir.
- **Ödeme yapılamadı**
- **Değiştirme siparişi oluşturuldu**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>E-posta şablonlarını belirli teslimat şekilleri için konfigüre et

Bu yordam için, yeni, özel e-posta şablonlarınızı oluşturmuş ve bunları **organizasyon e-posta şablonları sayfasına eklemiş olduğunuz varsayımıyla belirtilir**. E-posta şablonlarının nasıl oluşturulacağı ve karşıya yükleneceği hakkında bilgi için, bkz [İşlem olayları için e-posta şablonları oluşturun](email-templates-transactions.md).

Commerce Headquarters 'da belirli teslimat şekilleri için e-posta şablonlarını konfigüre etmek amacıyla aşağıdaki adımları izleyin.

1. **Commerce e-posta bildirim profili**'ne gidin.
1. **Perakende olay bildirimi ayarları**'nda, varolan bir bildirim türünü seçin.
1. Bildirim türü hala seçiliyken, **Teslimat şekillerini konfigüre et**'i seçin.
1. **Teslimat şekilleri** iletişim kutusunda, **Yeni**'yi seçin.
1. Yeni satırda **Teslimat şekli** alanında, teslimat şeklini seçin.
1. **E-posta kimliği** alanında, teslimat moduyla eşlenecek e-posta şablonunu seçin.
1. **Etkin** onay kutusunu işaretleyin.
1. Daha fazla teslimat şekli eklemek için 4 ile 7 arasındaki adımları yineleyin.
1. Tamamladıktan sonra **Tamam**'ı seçin.

> [!NOTE]
> - Bir satış siparişindeki satırlar arasında birden fazla teslimat modu varsa, varsayılan şablon kullanılacak. Varsayılan şablon, **Commerce e-posta bildirim profili** sayfasındaki bildirim türüyle eşlenen şablondur.
> - Satış siparişinin özel bir e-posta şablonu için konfigüre edilmemiş bir teslimat modu varsa, varsayılan e-posta şablonu kullanılır.

## <a name="additional-resources"></a>Ek kaynaklar

[Çağrı merkezi siparişleri oluşturma](tasks/create-call-center-orders.md)

[Satış noktasında teslimat şeklini değiştirme](pos-change-delivery-mode.md)
