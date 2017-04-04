---
title: "Sipariş son giriş tarihleri"
description: "Bu makalede sipariş giriş son tarihleri hakkında bilgiler verilmiştir. Bir sipariş girişi son tarihi, bir müşteri siparişinin o gün ya da ertesi gün alındığının kabul edilip edilmeyeceğini (ve yerine getirilip getirilmediğini) belirleyen bir kesim tarihidir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d865260679dac6196a69f3182f937df7f9fd8200
ms.lasthandoff: 03/31/2017


---

# <a name="order-entry-deadlines"></a>Sipariş son giriş tarihleri

Bu makalede sipariş giriş son tarihleri hakkında bilgiler verilmiştir. Bir sipariş girişi son tarihi, bir müşteri siparişinin o gün ya da ertesi gün alındığının kabul edilip edilmeyeceğini (ve yerine getirilip getirilmediğini) belirleyen bir kesim tarihidir.

Çoğu şirkette, günün yalnızca belirli bir saati öncesinde alınan satış siparişleri o gün alınmış sayılır. O saatten sonra alınan siparişler, sonraki işgünü alınmış sayılır. Siparişlerin sonlanacağı bu saate, son sipariş giriş saati denilir.  

Son sipariş giriş saatleri, sipariş vaatleri için bir girdi olarak kullanılırlar. Bu nedenle, müşterilerin sipariş teslimi konusundaki beklentilerini yönetmenize yardımcı olurlar. Örneğin, müşteriler belirli bir saatten önce size sipariş verdiklerinde malları aynı gün teslim etmeyi vaat ettiğinizi görebilirler. Ancak, bunlar o son kaçırırsanız, sevk irsaliyesi yalnızca sonraki iş günü bekleyebilirsiniz. Ambar yetenekleri ve kargo taşıyıcı zamanlamaları göre sipariş son giriş tarihleri ayarlayın.  

**Son sipariş giriş saatleri** sayfasında, haftanın tüm günleri için son sipariş giriş saati ayarlayın. Belirtilmiş o saatten sonra sipariş alınırsa, sonraki işgünü alınmış sayılır. Varsayılan olarak bu saatler ilgili günün gece yarısına bir dakika kalan 23:59 saatine ayarlanmıştır. Varsayılan saatleri, gerçek sevk tarihi veya giriş tarihi saatleriyle örtüşecek şekilde değiştirebilirsiniz.  

Belirli bir müşteri grubu için son sipariş giriş saati tanımlayabilirsiniz. Örneğin, belirli bir müşteri grubunun diğer müşterilerden daha geç son sipariş giriş saatlerine sahip olmasını isteyebilirsiniz. Bu durumda, önce son sipariş giriş saatleri için **Son sipariş giriş saati grupları** sayfasında gruplar tanımlayın. Ardından grupları **Müşteriler** sayfasındaki müşterilere atayın.  

Şirketiniz birkaç tesisten oluşuyorsa, her tesis için son sipariş giriş saatlerini ayarlayabilirsiniz. Tesisler farklı saat dilimlerinde bulunuyorsa, son sipariş giriş saati söz konusu tesisin saat diliminde ayarlanır. Ancak, satış siparişleri ve satış teklifleri ile çalışırken, son sipariş giriş saati **Mevcut sevk ve giriş tarihleri** sayfasındaki saat diliminize dönüştürülür.  

**Son sipariş giriş saat birleşimlerini etkinleştir** sayfasında, izin verilen tesis birleşimlerini ve son sipariş giriş saati gruplarını tanımlarsınız.

## <a name="example-order-entry-deadline"></a>Örnek: Son sipariş giriş saati
Son sipariş giriş saati, Salı günü 16:00 olarak ayarlandı. Belirli bir Salı günü saat 17:00'de, geçerli tarihi sevk tarihi olarak ayarlamaya çalışın. (Bu örnek lider zaman olduğunu unutmayın.) Yoksa **teslim tarihi kontrol** onay kutusu seçiliyse, tarihi geçerli olmadığını bildiren bir uyarı alırsınız. Bu uyarı, alternatif tarihler seçebileceğiniz **Mevcut sevk ve giriş tarihleri** sayfasında belirir.

## <a name="example-different-order-entry-deadlines-per-site"></a>Örnek: Her tesis için farklı son sipariş giriş saati
Şirketiniz iki tesisten oluşuyor. Tesisler, aşağıdaki tabloda gösterilen şekilde farklı saat dilimlerinde yer almaktadır.

| Tesis A                      | Tesis B                      |
|-----------------------------|-----------------------------|
| California                  | Florida                     |
| PST (Pasifik Standart Saati) | EST (Doğu Standart Saati) |

Tesis A ve B, aşağıdaki son sipariş giriş saatlerini tanımladılar.

| Haftanın günü             | A: sipariş son giriş tarihleri (PST) | B: sipariş son giriş tarihleri (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Pazartesi                      | 13:00                          | 14:00                          |
| Salı                     | 13:00                          | 14:00                          |
| Çarşamba                   | 13:00                          | 14:00                          |
| Perşembe                    | 13:00                          | 14:00                          |
| Cuma                      | 13:00                          | 14:00                          |

MST (Sıradağlar Standart Saati) saat diliminde yer alan Utah'ta bir sipariş işlemcisisiniz. Dolayısıyla bu, A tesisine MST 14:00'dan önce ve B sitesine MST 12:00'dan önce sipariş verdiğiniz sürece, her iki tesisin de son sipariş giriş saatlerine uygun davrandığınız anlamına gelir.  

Aşağıdaki tabloda A ve B tesisleri için MST saatine dönüştürülmüş son sipariş giriş saatleri gösterilir.

| Site A: PST         | Site A: MST        | Site B: EST           | Site B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 14:00                 | 12:00              |

**Not:** Yaz saati uygulaması devredeyse, son sipariş giriş saati ona göre ayarlanır.

## <a name="example-same-order-entry-deadline-per-site"></a>Örnek: Her tesiste aynı son sipariş giriş saati
Şirketiniz iki tesisten oluşuyor. Tesisler, aşağıdaki tabloda gösterilen şekilde farklı saat dilimlerinde yer almaktadır.

| Tesis A                      | Tesis B                      |
|-----------------------------|-----------------------------|
| California                  | Florida                     |
| PST (Pasifik Standart Saati) | EST (Doğu Standart Saati) |

Tesis A ve B, aşağıdaki son sipariş giriş saatlerini tanımladılar.

| Haftanın günü | PST ve EST |
|-----------------|-------------|
| Pazartesi          | 13:00       |
| Salı         | 13:00       |
| Çarşamba       | 13:00       |
| Perşembe        | 13:00       |
| Cuma          | 13:00       |

Bir sipariş işlemcisisiniz ve MST saat diliminde yer alan Utah'ta bulunuyorsunuz. Dolayısıyla bu, A tesisine MST 14:00'dan önce ve B sitesine MST 11:00'dan önce sipariş verdiğiniz sürece, her iki tesisin de son sipariş giriş saatlerine uygun davrandığınız anlamına gelir. 

Aşağıdaki tabloda A ve B tesisleri için MST saatine dönüştürülmüş son sipariş giriş saatleri gösterilir.

| Site A: PST         | Site A: MST        | Site B: EST           | Site B: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 13:00                 | 11:00              |

**Not:** Yaz saati uygulaması devredeyse, son sipariş giriş saati ona göre ayarlanır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Delivery schedules](delivery-schedules.md)


