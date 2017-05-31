---
title: "Ödendiğinde öde satıcı anlaşmaları"
description: "Bu makalede, satıcı anlaşmaları için ödendiğinde ödeme (PWP) koşulları açıklanmaktadır. PWP koşulları, bir müşteri size ödeme yapana kadar satıcıya ödemeyi kısmen veya tamamen bekletmenize olanak sağlar. Bu makalede PWP koşullarını bir proje için nasıl kullanacağınızı göstermek için gerçek yaşamdan bir örnek de verilmektedir."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23131
ms.assetid: 20bf1d7f-8813-4c69-9cd7-576884a7e169
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7b21d4e93ec22715d530b75f75f3ba475e561f62
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="pay-when-paid-vendor-agreements"></a>Ödendiğinde öde satıcı anlaşmaları

[!include[banner](../includes/banner.md)]


Bu makalede, satıcı anlaşmaları için ödendiğinde ödeme (PWP) koşulları açıklanmaktadır. PWP koşulları, bir müşteri size ödeme yapana kadar satıcıya ödemeyi kısmen veya tamamen bekletmenize olanak sağlar. Bu makalede PWP koşullarını bir proje için nasıl kullanacağınızı göstermek için gerçek yaşamdan bir örnek de verilmektedir.

Bir taşeron olarak bir proje üzerinde çalışmak için bir satıcıyı onayladığınızda, müşteriniz proje için ödeme yapana kadar satıcı veya taşerona ödemeyi yapmamak isteyebilirsiniz. Bir satıcıya ödeme stopajı uygulamak için, satıcı ile satınalma siparişini ayarladığınızda ödendiğinde öde (PWP) koşullarını ayarlayın. Satıcı için bir satınalma siparişi oluşturduğunuzda ve bu satınalma siparişine bir proje kodu atadığınızda, projedeki PWP şartları bu satınalma siparişi ve satıcı ile ilişkilendirilirler. **Ödendiğinde ödeme şartlı satıcı faturaları** sayfasında, bir satınalma siparişi için ödenmemiş satıcı faturalarının bir listesini ve ilişkili müşteri faturalarını görebilirsiniz. Bir satıcıya ne kadar ödeneceğini ve nasıl ödeme yapılacağını bu formu kullanarak belirleyin. Örneğin bir müşteri bir proje faturasındaki tutarı ödediğinde, ilgili satıcı faturalarının hepsini veya bir bölümünü ödeme için serbest bırakabilirsiniz. PWP şartlarını, satıcıya ancak ilgili ödemenin belirli bir miktarının müşteriden alındığında ödeme yapılacağını belirtecek şekilde ayarlayabilirsiniz. Bir müşteriden kısmi ödeme aldığınızda, ilgili bazı satıcı faturalarını ödeme için el ile serbest bırakabilirsiniz. Aşağıdaki örnek, müşterinin ödeme yapana kadar satıcı veya taşerona stopaj uygulanacak PWP koşullarını nasıl kullanabileceğinizi gösterir. Kuruluşunuz, müşteri ile, müşterinin talep ettiği yazılımları yükleyeceğiniz 100 bilgisayarı sağlamak üzere bir anlaşmaya girer. Sizin ve müşterinizin üzerinde anlaştığı fiyat her bilgisayar için 150,00'dir. Bilgisayarları sağlamak için bir üçüncü taraf satıcıdan hizmet alırsınız. Müşteri bilgisayarların kalitesini kuruluşunuza ödeme yapmadan önce onaylamak ister. Kuruluşunuzun ilkesi, müşteriden proje üzerindeki ödemeyi alana üçüncü parti satıcılara ödemeyi yapmamaktır. Bu nedenle, PWP yüzdesinin 100 olduğu bir proje ayarlarsınız. Böylece satıcıya gidecek tüm ödemeleri, müşteri faturasını tamamen kapatana kadar durdurursunuz. Her bilgisayar için satıcı tarafından 100,00 ücret alınır. Satıcı bilgisayarları size gönderdiğinde bu sevkiyata 100 bilgisayar için 10.000,00'lik bir fatura da dahildir. Projeyi PWP koşullarla ayarlamış olduğunuz için satıcıya ödeme yapmazsınız. Bilgisayarları satıcıdan aldıktan sonra, talep edilen yazılımları bilgisayarlara yüklersiniz. Bilgisayarları müşteriye gönderdiğinizde, 15.000,00'lik fatura da müşteriye gönderilir. Müşteri bilgisayarları inceler ve ürünün kalitesini onaylar. Daha sonra müşteri kuruluşunuza proje fatuasının toplam tutarını öder. Müşteriden tam ödemeyi almanızdan sonra, satıcıya, satıcı faturasının toplam miktarı olan 10.000,00'i ödersiniz.




