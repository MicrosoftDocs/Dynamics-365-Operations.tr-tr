---
title: Varış yeri maliyeti için eklenen satırı ayarları
description: Bu konuda, Varış yeri maliyeti modülünü etkinleştirdiğinizde var olan Satıcılar sayfasına eklenen yeni alanlar açıklanmaktadır. Bu alanları, Varış yeri maliyeti özellikleriyle birlikte kullanacağınız satıcıları ayarlamak için kullanırsınız.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b4e02397f7a4cdeaa21b451268b16e4fbe773612
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690540"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Varış yeri maliyeti için eklenen satırı ayarları

[!include [banner](../../includes/banner.md)]

**Varış yeri maliyeti** modülünü etkinleştirdiğinizde, var olan **Satıcılar** sayfasına birkaç yeni alan eklenir. Bu alanları, Varış yeri maliyeti özellikleriyle birlikte kullanacağınız satıcıları ayarlamak için kullanırsınız.

İlgili alanları ayarlamak için **Satın alma ve tedarik \> Satıcılar \> Tüm satıcılar**'a gidin. Var olan bir satıcıyı açın veya yeni bir satıcı oluşturun ve **Çeşitli ayrıntılar** hızlı sekmesini seçin. **Varış yeri maliyeti** modülünün eklediği tüm yeni alanlar **Seyahatler** başlığı altında görünür. Aşağıdaki tablo bu alanları açıklar.

| Alan | Tanım |
|---|---|
| Sevkiyat türü | <p>Satıcının Varış yeri maliyeti ile ilgili rolünü seçin:</p><ul><li>**Yok**: Satıcının Varış yeri maliyeti ile ilgili belirli bir rolü yoktur. Bu değer varsayılan ayardır çünkü çoğu satıcının büyük olasılıkla belirli bir rolü olmayacaktır.</li><li>**Sevkiyat şirketi**: Satıcı bir sevkiyat şirketidir. Bu sevkiyat türüne sahip satıcılar, **Seyahatler** sayfasındaki **Sevkiyat şirketi** alanında seçim için kullanılabilir.</li><li>**Gümrük müşaviri**: Satıcı bir gümrük müşaviridir. Bu sevkiyat türüne sahip satıcılar, **Folyolar** sayfasındaki **Gümrük müşaviri** alanında seçim için kullanılabilir.</li><li>**Aracı**: Satıcı bir aracıdır. Bu sevkiyat türüne sahip satıcılar, **Satıcılar** ve **Satın alma siparişleri** sayfalarındaki **Aracı** alanında seçim için kullanılabilir.</li></ul> |
| Maliyet türü grubu | [Otomatik maliyetleri](auto-cost-setup.md) seçmek amacıyla satıcıyı bir maliyet türü grubuna atayın. |
| Çıkış limanı | Seyahat için çıkış limanını seçin. |
| Temsilci | Satıcıdan satın alma yapıldığında varsayılan aracı. |
| İthalat maliyetlendirme satıcısı | <p>Satıcının Varış yeri maliyeti satıcısı olup olmadığını belirtin.</p><p>**İpucu:** Bir seyahat oluşturulduğunda gösterilen satın alma siparişlerini sınırlamak için bu alanı kayıt düzeyinde güvenlikle birlikte kullanabilirsiniz.</p> |
| Sevkiyat şirketi | Satıcı için satın alma siparişleri oluşturulduğunda kullanılan varsayılan sevkiyat şirketini seçin. |
| Hizmet sağlayıcı | Satıcının hizmet sağlayıcısı olup olmadığını belirtin. |
| Fazla/Eksik toleransı grubu | Satıcı için varsayılan fazla/eksik tolerans grubunu seçin. |
