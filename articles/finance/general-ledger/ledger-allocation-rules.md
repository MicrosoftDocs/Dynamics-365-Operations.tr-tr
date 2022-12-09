---
title: Genel muhasebe tahsisat kuralları
description: Bu makalede genel muhasebe atama kuralları hakkında bilgiler sağlanmıştır. Bu atama kurallarının çeşitli bileşenleri ve bunlar için kullanılabilecek atama yöntemleri açıklanmıştır.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: kfend
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0691c65e6a499f713952070811cefaa7a213af7b
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787566"
---
# <a name="ledger-allocation-rules"></a>Genel muhasebe tahsisat kuralları

[!include [banner](../includes/banner.md)]

Bu makalede genel muhasebe atama kuralları hakkında bilgiler sağlanmıştır. Bu atama kurallarının çeşitli bileşenleri ve bunlar için kullanılabilecek atama yöntemleri açıklanmıştır.

Genel muhasebe tahsisat kuralları, otomatik olarak hesaplama yapmak ve sabit tutarların veya genel muhasebe bakiyelerinin tahsisatı için tahsisat günlükleri ve hesap girişleri oluşturmak için kullanılır. Tahsisat yöntemleri, değişken veya sabit olabilir. Tahsisat, hareket para birimi değerine dayalı olarak yapılır. Örneğin, muhasebe ve raporlama para birimi tutarlarını ayarlamak için yabancı para birimi kazanç/zarar hesabı girişleri deftere nakledilir. Bu girişler, hareket para birimi değeri 0,00 olduğundan tahsisat kurallarına tabi değildir. Aşağıdaki tahsisat yöntemleri genel muhasebe tahsisat kuralları için kullanılabilir:

-   **Temel** – Bu değişken yöntemi, tahsisat, filtre ölçütü temel alınarak fiili genel muhasebe bakiyesine bağlı olduğunda kullanılır. Örneğin, reklamcılık giderleri tüm departman satışlarının toplam departman satışlarına oranına dayalı olarak tahsis edilebilir.
-   **Sabit yüzde** ve **Sabit ağırlık** – Bu yöntemler için, tahsisat yüzdesi veya ağırlığı doğrudan kural için tanımlanır. Örneğin, reklam giderleri reklam giderlerinin yüzde 70'ini Departman A ve yüzde 30'unu Departman B alacak şekilde tahsis edilebilir.
-   **Eşit olarak** – Bu yöntem, tutarları tanımlanan her bir hedefe eşit olarak dağıtır. Örneğin, Departman A ve Departman B için hedefler tanımlandıysa, reklam giderleri hem Departman A hem de Departman B giderlerin yüzde 50'sini alacak şekilde tahsis edilebilir.

Bir tahsisat kuralının tahsisat yöntemi olarak Temel kullanılırsa, başka bir temel genel muhasebe tahsisat kuralları da oluşturmanız gerekir. "Tahsisat talebini işleme koy" işlemi kullanıcıların genel muhasebe kuralını işleme almasını ve hesaplanmış tahsisatları deftere nakletmeden ya da silmeden önce ortaya çıkan günlük girişlerini önizlemelerini sağlar.

## <a name="components-of-ledger-allocation-rules"></a>Genel muhasebe tahsisat kuralları bileşenleri
Her tahsisat kuralının dört bileşenini vardır: Genel, kaynak, hedef ve mahsup. Tahsisat yöntemi olarak Temel kullanılıyorsa, ek bir bileşen ve genel muhasebe tahsisat kuralları gereklidir. Her bir bileşen tahsisatları işleme almak için gerekli bilgilerin önemli bir kısmını sağlar.

-   **Genel** – Bu bileşen; tahsisat yöntemi, şirketlerarası kural ayarı ve kuralın etkin olup olmadığı gibi seçenekleri belirlediği yerdir.
-   **Kaynak** – Bu bileşen; kullanıcının tahsisat için veri kaynaklarını belirlediği yerdir. Tahsisat, genel muhasebeye (**Veri kaynağı** =  **Genel muhasebe**) veya sabit tutarlara (**Veri kaynağı** =  **Sabit değer**) dayalı olabilir. **Veri kaynağı**, **Genel muhasebe** olarak ayarlandığında, kaynak filtresi ölçütünün genel muhasebe kuralı için (örneğin reklam giderleri için) tanımlanması gerekir.
-   **Hedef** – Bu bileşen, tahsisat sonucunun nasıl dağıtılacağını ve hesaplanacağını tanımlar. Örneğin, her departman için bir hedef satır olabilir.
-   **Mahsup** – Bu bileşen, ana hesapların ve boyutların bakiye hedef girişleri için nasıl belirlenmesi gerektiğini tanımlar. Kullanıcı tanımlı seçenekler genellikle kaynağa dayalı hesapların ve boyutların yerine kullanılır. **Veri kaynağı** **Sabit değer** olarak ayarlandığında, **Kaynak** bir seçenek olarak kullanılamaz.
-   **Temel genel muhasebe kuralları** – Bu kurallar, tahsisat için hangi genel muhasebe bakiyesinin (örneğin, departman başına gelir) kullanılması gerektiğini belirlemek için kullanılır. Her bir genel tahsisat kuralı birden çok tahsisat kuralıyla birlikte kullanılabilir.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
