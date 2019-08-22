---
title: Tedarik kategorisi hiyerarşileri için ilkeler ayarlama
description: Bir kategorideki ürünleri sipariş etmek amacıyla kuralları ayarlamak için bu prosedürü kullanın.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 230794eacd5e9911496dd3826f08126cc21494cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844189"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Tedarik kategorisi hiyerarşileri için ilkeler ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bir kategorideki ürünleri sipariş etmek amacıyla kuralları ayarlamak için bu prosedürü kullanın. Kurallar belirli bir satın alma ilkesi için tanımlanır. Kategori erişimi kuralı, talep oluşturulduğunda hangi tedarik kategorisi çalışanlarının erişime sahip olacağını denetler. Bir talep oluşturulduktan sonra uygulanması gereken satınalma ilkesi ve kategori erişim kuralı çalışanların bağlı olduğu tüzel kişilik ve işletme birimi tarafından belirlenir. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Genellikle bu görev bir satınalma yöneticisi tarafından gerçekleştirilir.


## <a name="find-the-procurement-policy"></a>Tedarik ilkesini bulun
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Ayar > İlkeler > Satınalma ilkeleri**'ne gidin.
2. "Tedarik İlkesi USMF"deki bağlantıya tıklayın. Bu, kuralı ekleyeceğiniz ilkedir. Etkin ilke olması gerekir.  

## <a name="create-a-category-access-rule"></a>Kategori erişimi kuralı oluşturun
1. **İlke kuralları** hızlı sekmesini genişletin.
2. **İlke kuralı türü** listesinde, **Kategori erişim ilkesi kuralını**seçin. **İlke kuralı oluştur** düğmesi soluk görünüyorsa bunun nedeni Kategori erişimi için zaten etkin bir ilke kuralının olmasıdır. Hangisi olduğunu belirlemek için **Yürürlük** ve **Bitiş** tarihi alanlarını işaretleyin, sonra seçin ve **İlke kuralını kullanımdan kaldır**'a tıklayın. **İlke kuralı oluştur** düğmesi kullanılabilir durumdaysa başka bir işlem yapmanız gerekmez.  
3. **İlke kuralı oluştur** öğesine tıklayın.
4. **Yürürlük tarihi** alanına bir tarih ve saat girin. Süre zaten etkin olan başka bir kuralla çakışmamalıdır.  
5. Kuralın uygulanacağı bir kategori seçin. Bunun hangi kategori olduğunu not edin, daha sonra ihtiyacınız olacak. Bir kategori seçtiğinizde, üst kategorisi veya kategorileri de Seçili kategoriler listesine eklenecektir. Kuralı seçili kategorinin tüm alt kategorilerine uygulamak istiyorsanız **Alt kategorileri dahil et** onay kutusunu seçin.
6. **Seçili kategoriler** listesine eklemek için sağ oku tıklatın.  
4. **Tamam**'a tıklayın. **Üst kuralı dahil et** seçeneğini Evet olarak ayarlarsanız üst kategori için tanımladığınız ilke kuralı, alt kategoriler için ilke kuralı tanımlanmamışsa alt kategorilerine de atanır.

## <a name="create-a-category-policy-rule"></a>Kategori ilkesi kuralı oluşturun
1. **İlke kuralı türü** listesinde, **Kategori ilkesi kuralını**seçin. **İlke kuralı oluştur** düğmesi soluksa etkin ilke kuralını seçin ve **İlke kuralını kullanımdan kaldır**'a tıklayın.  
2. **İlke kuralı oluştur** öğesine tıklayın.
3. **Yürürlük tarihi** alanına bir tarih ve saat girin.
4. **Ekle** öğesine tıklayın.
5. **Kategori** alanında, **Kategori erişimi kuralı** için kullandığınız aynı kategoriyi seçin.
6. **Satıcı seçimi** alanında, bir seçenek belirleyin. Talepler oluşturulduğunda kategori için hangi tür satıcıların seçilebileceğini denetleyen bir kural seçin.  
7. **Kapat**'a tıklayın. Tanımladığınız ilke kuralları Tüketim türü talepleri içindir. Stok yenileme türü talepleri için ilkeleri tanımlamak isterseniz "Stok yenileme kategorisi erişim ilkesi kuralı" olarak adlandırılan İlke kuralı türü için bir kural oluşturursunuz.  

