---
title: Pozisyonlar
description: Bu konu, bir pozisyonun içerebileceği kavramsal öğeleri açıklar. Kuruluşunuzda bu öğeleri nasıl kullanabileceğinizi gösteren örnekler de sağlar.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 95abd7548d23ef1b4f5fc31ebaa818e06e179d60
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068831"
---
# <a name="positions"></a>Pozisyonlar


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, bir pozisyonun içerebileceği kavramsal öğeleri açıklar. Kuruluşunuzda bu öğeleri nasıl kullanabileceğinizi gösteren örnekler de sağlar.

Pozisyon oluşturabilmeniz için bir iş ayarlanmış olması gerekir. Ücret bölgesi, çalışan ataması, pozisyon süresi ve raporlama ilişkisi gibi bazı pozisyon ayrıntıları için yürürlük tarihi bulunur.

## <a name="general-information"></a>Genel bilgiler

Pozisyon oluşturduğunuzda, bir iş seçmeniz gerekir. Aşağıdaki bilgiler seçtiğiniz işten otomatik olarak doldurulacaktır:

- Tanım
- Unvan
- Tam zamanlı eşdeğeri
- İş ailesi

Pozisyon unvanı bir çalışanın unvanına başvurmak için kullanılır. (Çalışanda listelenen unvan kullanılmaz.) Bu nedenle, konum unvanları mümkün olduğunca standartlaştırılmış olmalıdır.

> [!NOTE]
> Bir çalışan, atama için uygun olma tarihinden önceki bir tarihte bir pozisyona atanamaz.
>
> **İnsan kaynakları paylaşılan parametreleri** sayfasının **Pozisyonlar** sekmesindeki bir parametre, çalışan atama davranışını denetler. Aşağıdaki değerlerden birini seçin:
>
> - **Her zaman** – Pozisyonlar oluşturulurken çalışanları yeni pozisyonlara atayamazsınız. Pozisyonlar oluşturulurken, **Pozisyon** sayfasının **Genel** sekmesindeki **Atama için kullanılabilir** tarih ve saat, oluşturma tarihi ve saatine otomatik olarak ayarlanır.
> - **Hiçbir zaman** – pozisyonlar oluşturduğunuzda yeni konumlara çalışanları atayamazsınız. Bu seçeneği seçerseniz, her yeni pozisyon kullanılabilir hale geldiğinde **Pozisyon** sayfasını açmanız gerekir. Daha sonra, **Genel** sekmesinde, çalışan atamasını etkinleştirmek üzere **Atama için kullanılabilir** tarihini girin. Bu seçeneği belirlerseniz, çalışanı atamaya çalıştığınızda çalışan atama tarihi varsayılan olarak **Hiçbir zaman** olarak ayarlanır.

## <a name="position-duration"></a>Pozisyon süresi

Her pozisyon, süre olarak başvurulan belirli bir süre boyunca geçerlidir. Örneğin, yaz pozisyonları 1 Mayıs 2021'ten 31 Ağustos 2021'e kadar bir süreye sahip olabilir. Etkinleştirme tarihi, sistemde pozisyonun etkin olduğu tarihtir. Geri çekme tarihi, sistemde pozisyonun artık etkin olmadığı tarihtir.

Atama için kullanılabilir tarihinin ve çalışan atama tarihinin etkinleştirme tarihinden önce olamayacağını dikkate alın. Etkinleştirme tarihine ulaşılıncaya kadar bir pozisyon etkin kabul edilmez. Ek olarak, bir çalışan ataması pozisyonun geri çekilme tarihinden sonraya uzatılamaz.

## <a name="reports-to-position"></a>Rapor verilen pozisyon

Pozisyonlar, bir kuruluş hiyerarşisinin alt düzeyi için önemli öğelerdir. **Pozisyon** sayfasında, bir pozisyonun rapor vereceği pozisyonu belirtebilirsiniz. Bir pozisyona başka bir pozisyona rapor veren bir işçi atadığınızda, iki pozisyona atanan işçiler arasında bir raporlama ilişkisi oluşturmuş olursunuz. Örneğin, 000220 pozisyonu 000300 pozisyonuna rapor verir. Kim Akers 000220 pozisyonuna atanmıştır ve Sanjay Patel 000300 pozisyonuna atanmıştır. Bu nedenle, Kim Akers Sanjay Patel'e rapor verir.

> [!TIP]
> Bir çalışanın yöneticisinin kim olduğunu belirlemek için, rapor verilecek pozisyon tüm sistemde kullanılır. Önceki örnekte, sistemde yönetici rolü Sanjay Patel'e atanırsa, Yönetici Self Servisinde Kim Akers'i doğrudan rapor veren bağlı çalışan olarak görür. Raporlama ilişkisi, iş akışı yönlendirme kuralları ve denetim listesi görevleri oluştururken de kullanılabilir.

## <a name="relationships"></a>İlişkiler

Kuruluşunuzda bir matris hiyerarşisi veya başka bir özel hiyerarşi kullanılıyorsa, pozisyon hiyerarşi türleri ayarlayabilirsiniz. Sonra, ayarladığınız her hiyerarşi türü için pozisyonlara raporlama ilişkileri ekleyebilirsiniz. Örneğin, Lori Penor Adventure Works'te genel müdürdür ve **Genel Müdür** pozisyonuna atanmıştır. Lori ıvır zıvır temizliğinde kullanılan bir ürünün geliştirilmesini yönetmektedir. Mali konularda yardımcı olması için bir muhasebeciye ihtiyacı vardır. Bu nedenle, Kim Akers'i muhasebecisi olarak işe almıştır. Kim, doğrudan Sanjay Patel'e rapor vermektedir ancak arabirim öğesi temizleyici geliştirme çalışmasının finansmanı konusunda Lori Penor ile birlikte de çalışır.

Önceki örnek için, Kim Akers ve Lori Penor arasında iş ilişkisi oluşturacak aşağıdaki görevleri tamamlamanız gerekir:

1. Arabirim öğesi temizleme ürünü üzerinde çalışmaktan sorumlu olan pozisyonları içeren bir hiyerarşi yaratmak için **Arabirim öğesi** adlı özel bir pozisyon hiyerarşisi türü oluşturun.
2. **Genel Müdür** pozisyonunu, Kim'in **Arabirim öğesi** hiyerarşisinde rapor vereceği pozisyon olacak şekilde belirtin.
3. Pozisyon hiyerarşisini kullanarak pozisyonların raporlama yapısını görüntüleyin. Birden fazla pozisyon hiyerarşiniz varsa, pozisyon hiyerarşisindeki her bir hiyerarşi türü için hiyerarşileri görüntüleyebilirsiniz. Bir pozisyonu, pozisyon koduna veya o pozisyona atanan işçinin adına göre aratabilirsiniz. Pozisyon hiyerarşisi bir organizasyon hiyerarşisidir.

## <a name="labor-union"></a>Sendika

Pozisyon için bir sendika sözleşmesinin gerekli olup olmadığını ve hangi iş sendikasının kullanıldığını kaydedebilirsiniz. Ayrıca, sözleşmeyi tüzel bir kişilikle ilişkilendirebilirsiniz.

## <a name="financial-dimensions"></a>Mali boyutlar

Bir pozisyon için mali boyut oluşturduğunuzda, geçerli bir tüzel kişilik belirtmeniz gerekir. Her bir boyut için varsayılan boyutları bağımsız olarak seçebilirsiniz. Alternatif olarak, varsayılan boyutları otomatik olarak doldurmak için bir dağıtım şablonu seçebilirsiniz. Dağıtım şablonu aynı zamanda çoklu boyut değerleri arasında tutar tahsis etme seçeneği de sunar.
