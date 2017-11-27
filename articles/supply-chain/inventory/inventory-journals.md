---
title: "Stok günlükleri"
description: "Bu makalede, çeşitli fiziksel stok hareketi türlerini deftere nakletmek için stok günlüklerini nasıl kullanabileceğiniz açıklanmaktadır."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 968bf9a243d0c0cc9f0dfec474cb207ca32f9eeb
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-journals"></a>Stok günlükleri

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Bu makalede, çeşitli fiziksel stok hareketi türlerini deftere nakletmek için stok günlüklerini nasıl kullanabileceğiniz açıklanmaktadır.

Microsoft Dynamics 365 for Finance and Operations stok günlükleri çeşitli türdeki fiziksel stok hareketlerini deftere nakletmek için kullanılır, örneğin sorunlar ve girişler, stok hareketleri, ürün reçeteleri (BOM) oluşturulması ve fiziksel envanter mutabakatı deftere nakilleri gibi. Tüm stok günlükleri benzer şekilde kullanılır, ancak bunlar farklı türlere ayrılır.

## <a name="types-of-inventory-journals"></a>Stok günlükleri türleri
Kullanılabilen stok günlükleri türleri şunlardır:

-   Hareket
-   Stok düzeltmesi
-   Transfer et
-   Ürün reçetesi
-   Madde varışı
-   Üretim girişi
-   Sayım
-   Etiket sayımı

### <a name="movement"></a>Hareket

Bir stok hareketi günlük kullandığınızda, stok eklemek, ancak el ile günlüğü oluşturduğunuzda, genel muhasebe mahsup hesabı belirterek belirli bir genel muhasebe hesabı için ek maliyet ayırmalıdır maliyet bir öğeye ekleyebilirsiniz. Bu stok günlüğü türü, öğenin farklı bir bölüme karşı gider olarak göstermek istiyorsanız veya öğeleri gider amacıyla stoktan kaldırmak istiyorsanız yararlıdır.

### <a name="inventory-adjustment"></a>Stok düzeltmesi

Bir stok ayarlama günlüğü kullandığınızda, stok eklediğinizde, bir öğeye maliyet ekleyebilirsiniz. Ek maliyet belirli bir genel muhasebe defter hesabına, nakil profili madde grubunun kurulumu temel alınarak otomatik olarak nakledilir. Bu stok günlüğü tipini madde kendi varsayılan genel muhasebe mahsup hesabı tutacaksa, kazanç ve kayıplar için stok miktarlarını güncelleştirmek için kullanın. Bir stok düzeltme günlüğü naklettiğinizde stok girişi veya çıkışı nakledilir, stok değerleri değiştirilir ve genel muhasebe hareketleri oluşturulur.

### <a name="transfer"></a>Transfer et

Transfer günlükleri, herhangi bir maliyet etkileri ilişkilendirme olmadan öğeleri stoklama konumları, toplu işlem veya ürün çeşitleri arasında aktarmak için kullanabilirsiniz. Örneğin, aynı şirket içinde bir ambardan başka bir ambardan öğeleri aktarabilirsiniz. Bir transfer günlüğü kullandığınızda, "kaynak" ve "hedef" stok boyutlarının (örneğin, tesis ve ambar) her ikisini de belirtmelisiniz. Tanımlanan stok boyutları için eldeki stok uygun şekilde değiştirilir. Stok aktarımları, malzemenin hemen hareketlerini yansıtır. Transit stok izlenmez. Transit stok izlenmek zorundaysa, transfer emri kullanmalısınız. Transfer günlüğünü deftere naklettiğinizde, her günlük satırı için iki stok hareketi oluşturulur:

-   "Kaynak" konumundaki bir stok çıkışı
-   "Hedef" konumundaki bir stok girişi

### <a name="bom"></a>Ürün reçetesi

Bir ürün reçetesini tamamlandı olarak bildirdiğinde, ÜR günlüğü oluşturabilirsiniz. Bir ÜR günlüğü kullanarak, ürün reçetesini doğrudan deftere nakledebilirsiniz. Bu nakil ilişkili bir ürün reçetesi ve ürün Reçetesine dahil ürünlerin stok çıkışı ile birlikte ürünün stok girişini oluşturur. Bu stok günlüğü tipi, yolların gerekli olmadığı basit veya yüksek hacimli üretim senaryolarında faydalıdır.

### <a name="item-arrival"></a>Madde varışı

Madde varış günlüğünü, (örneğin, satınalma siparişlerindeki) maddelerin girişini kaydetmek için kullanabilirsiniz. Bir madde varış günlüğü **Varış genel bakış** sayfasından varış yönetiminin bir parçası olarak veya **Madde varış** sayfasından bir günlük girdisini el ile oluşturabilirsiniz. Malzeme çekme konumları denetlemek için madde varış günlüğü adını etkinleştirirseniz, Finance and Operations alınan maddeler için bir yerleşim arar ve yer mevcut ise gelen maddeler için konum hedefleri oluşturur.

### <a name="production-input"></a>Üretim girişi

Üretim girdi günlükleri madde varış günlüğü gibi çalışır, ancak üretim emirleri için kullanılır.

### <a name="counting"></a>Sayım

Sayım günlükleri madde veya madde grupları için eldeki stok miktarını düzeltmenize yardımcı olur ve böylece farkları bağdaştırmak için gerekli ayarları yapıp gerçek fiziksel sayımları deftere nakletmenizi sağlar. Sayım ilkelerini çeşitli özelliklere sahip öğeleri gruplamak amacıyla sayım grupları ile ilişkilendirebilirsiniz ve böylece bu maddeler de sayım günlüğüne dahil edilirler. Örneğin, sayım gruplarını belirli bir sıklığa sahip maddelerin sayımına ya da stok belirli bir düzeye düştüğünde maddelerin sayımını gerçekleştirecek şekilde ayarlayabilirsiniz. Sayım grupları tanımlama hakkında bilgi için bkz. [Stok sayım işlemlerini tanımlama (Görev kılavuzu)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Etiket sayımı

Etiket sayım günlükleri, numaralı bir etiketi lot sayımına atamak için kullanılır. Etiketin bir etiket numarası, madde numarası ve madde miktarı içermesi gerekir. Bir etiketin yalnızca bir kere ve tüm etiketlerin kullanıldığına emin olmaya yardımcı olmak için, her öğe numarasının kendi numara serisi olan bir dizi benzersiz etikete sahip olması gerekir. Her etiket için üç durum değerlerini ayarlayabilirsiniz:

-   **Kullanılan** – Bu etiket için madde numarası sayılır.
-   **Hükümsüz** – Bu etiket için madde numarası hükümsüz olur.
-   **Eksik** – Bu etiket için madde numarası eksiktir.

Bir etiket sayımı günlüğü naklederken, etiket sayım günlüğü satırlarına dayanan yeni bir sayım günlüğü oluşturulur. Etiket sayımı hakkında daha fazla bilgi için bkz. [Stok etiketi sayımı](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Günlüklerle çalışma.
Günlüğe bir defada yalnızca bir kullanıcı tarafından erişebilir. Günlük satırlarını oluşturmak için aynı anda birkaç kullanıcının günlüklere erişmesi gerekiyorsa, bilgi üzerine yazılmasını önlemek için bu kullanıcılar şu anda kullanılmayan günlükleri seçmesi gerekir. Birden fazla departmanın aynı günlük türünü kullandığı durumlarda, çok sayıda günlük adı oluşturmak (örneğin her departman için bir tane) yararlıdır. Her nakil yordamının kendi benzersiz stok günlüğüne girilmesi için günlükleri bölmek de yardımcı olabilir. Stok hareketleriyle ilişkili nakil yordamları için, periyodik stok düzeltmeleri için bir günlük, stok sayımı için de başka bir günlük oluşturun.

## <a name="posting-journal-lines"></a>Günlük satırlarını deftere nakletmek
Oluşturduğunuz günlük satırlarını istediğiniz zaman, bir öğe için ek hareketleri kilitleyene kadar deftere nakledebilirsiniz. Günlüğe girdiğiniz veriler günlükte, günlük satırları deftere nakletmeden kapatırsanız bile kalır.

