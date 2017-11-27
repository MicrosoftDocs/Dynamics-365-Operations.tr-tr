---
title: "Tedarik katalogları"
description: "Bu makalede yüksek bir düzeyde, satın alma uzmanlarının satın alma kataloglarını nasıl kurabilecekleri ve tutabilecekleri açıklanmıştır. Tedarik katalogları, şirket çalışanlarının şirket içi kullanım için sipariş edebileceği maddeleri ve hizmetleri tanımlar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f51fb41e19a47a9db02166de91b9e027154d6a7d
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-catalogs"></a>Tedarik katalogları

[!include[banner](../includes/banner.md)]


Bu makalede yüksek bir düzeyde, satın alma uzmanlarının satın alma kataloglarını nasıl kurabilecekleri ve tutabilecekleri açıklanmıştır. Tedarik katalogları, şirket çalışanlarının şirket içi kullanım için sipariş edebileceği maddeleri ve hizmetleri tanımlar.

Satınalma uzmanları bir kuruluşta dahili kullanım için satın alınabilir ürün ve hizmetlerin bir kataloğunu oluşturabilir ve sürdürebilir. Kataloglar ayarlandıktan sonra, şirket çalışanları bunlardan sipariş vermek için satınalma talepleri oluşturabilir. Çalışanların yalnızca satın alma tüzel kişiliği için izin verilen ürün ve hizmetleri sipariş edebilmesi için satın alma ilkelerini zorlamak üzere kataloglar kullanılabilir. Bir tedarik kataloğu oluşturduğunuzda aşağıdaki görevleri dikkate almanız gerekir:

-   Katalog oluşturmadan önce tedarik kategori hiyerarşinizi yapılandırın.
-   Personelinizin hangi ürünleri sipariş verebilmelerini istediğinizi belirleyin. Belirli ürünleri katalog düğümünde gösterebilir veya gizleyebilir ya da tüm ürünleri bir düğümde gizleyebilir veya gösterebilirsiniz.
-   Kaç adet tedarik kataloğuna ihtiyacınız olduğunu belirleyin. Tedarik kataloğuna erişim, tüzel ve bir kişilik için yapılandırdığınız katalog ilkesi kuralına ve bir çalışanın atandığı faaliyet birimine göre belirlenir.

Bir satınalma talebi oluşturduklarında çalışanların sipariş edebileceği ürünleri ve kullanabilecekleri tedarik kategorilerini şu gibi çeşitli faktörler belirler:

-   Satın alma ilkesindeki kategori erişimi ilkesi kuralı, hangi tedarik kategorilerinin satınalma talebinde kullanılabileceğini belirler. Tanımlı bir kural yoksa, tüm tedarik kategorileri kullanılabilir.
-   Çalışanlar yalnızca kuruluşunuz için etkin bir tedarik kataloğunda varsa ve düğümde etkin ve gizli değilse bir ürünü sipariş edebilir. Ürün aynı zamanda belirli bir çalışanın kategori erişimi ilkesi kuralına göre erişiminin bulunduğu bir kategoride olmalıdır.
-   Katalog ilkesi kuralı, kullanılan kataloğu belirtir. Tanımlanmış bir katalog ilkesi kuralı yoksa, kategori erişim kuralı çalışanın talebinde sipariş edebileceği ürünleri tek başına belirler.

## <a name="prerequisites"></a>Önkoşullar
Aşağıdaki tabloda, bir satın alma uzmanının tedarik kataloğu oluşturabilmesi için tamamlanması gereken görevler açıklanmaktadır.

| Görev                                                | Rol               | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bir tedarik kategori hiyerarşisi ayarlayın.            | Satınalma müdürü | Tedarik kategori hiyerarşileri, raporlama ve çözümleme amacıyla ürünleri veya hareketleri sınıflandırır. Bir tedarik kategori hiyerarşisi kullanarak, şirketler kategorileri, ürünleri, satıcıları ve diğer tedarik faktörlerini merkezi bir konumdan stratejik bir şekilde yönetebilir. Bir tedarik kategori hiyerarşisi kuruluşun tamamı için tanımlanır. Katalog, tedarik kategori hiyerarşisine dayalıdır: Hiyerarşideki kategoriler kataloğun düğümleri haline gelir. Satıcı ve ürünler kataloğunuza dahil edilir. |
| Satıcıları ve ürünleri tedarik kategorilerine ekleyin. | Satınalma müdürü | Kuruluşunuz için tedarik kategori hiyerarşisi oluşturulduğunda, her tedarik kategorisi belirli satıcılar, ürünler ve benzeri ile ilişkilendirilebilir. Bu ilişkiler otomatik olarak kataloğa kopyalanır.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Bir kataloğu ayarlama
Önkoşullar karşılandıktan sonra katalogları ayarlayabilirsiniz. Kuruluşunuzun tamamında kullanılan tek bir katalog veya kuruluşunuzdaki çeşitli bölümlerin kullandığı birden çok katalog oluşturabilirsiniz. Kuruluşun tamamı için tek bir katalog oluşturmak istiyorsanız, katalog satın alma İlkesi kurallarınız tarafından denetlenir.  

Katalog, satınalma talepleri oluşturulduğunda hangi ürünün kullanılabilir olacağını tanımlar, ancak ek kısıtlamalar uygulamak için kategori erişim ilkeleri kurallarını kullanabilirsiniz. Katalogdaki düğümler tedarik kategorileri olduğundan, bir kategori erişimi ilkesi kuralı tarafından kaldırılabilir. Bu durumda, o kategorideki ürünler çalışanlar tarafından taleplerde kullanılamaz. Kategori erişimi ilke kurallarını **Satınalma ilkeleri** sayfasında tanımlarsınız. Aşağıdaki tabloda bir kataloğu ayarlamak için tamamlanması gereken görevler açıklanmaktadır.

| Görev                                                   | Rol             | Açıklama                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yeni bir katalog oluşturun.                                  | Satınalma aracısı | Bir katalog oluşturduğunuzda, katalog içni bir ad ve açıklama belirtirsiniz. Ayrıca, kataloğun el ile mi yoksa otomatik olarak mı güncelleneceğini tanımlar ve katalog sahibini belirtirsiniz.                                                                                                                                      |
| Ürünlerin katalogda kullanılabilir olup olmadığını denetleyin. | Satınalma aracısı | Ürünler tedarik kategorilerden devralındığından, tüm uygun katalog düğümlerinde görünürler. Katalog bir satınalma talebinde kullanıldığında, bir düğümdeki tüm ürünlerin gizli mi yoksa görünür mü olduğunu denetleyebilirsiniz. Ayrıca, bir düğümdeki tek tek ürünlerin gizli mi yoksa görünür mü olacağını da denetleyebilirsiniz. |
| Kataloğu yayınlayın.                                   | Satınalma aracısı | Bir kataloğun çalışanların bir talepte kullanımı için uygun olması için kataloğun katalog ilke kuralını tanımlamanız ve katalog durumunu **Etkin** olarak ayarlayarak kataloğu yayınlamanız gerekir. Artık kullanıcılarınız için uygun olmamasını istediğiniz katalogları devre dışı bırakabilirsiniz.                                              |

Güncellemeler, **Katalog** sayfasında **Varsayılan güncelleme türü** alanında katalog için belirlediğiniz seçeneğe bağlı olarak otomatik olarak ya da el ile yayınlanır. Aşağıdaki varsayılan güncelleme türleri kataloglar için kullanılabilir:

-   **Dinamik** – Katalog her değiştiğinde otomatik olarak güncellenir.
-   **Statik** – Kataloglar el ile güncellenmelidir.
-   **Her ikisi** – Katalog, **Statik** varsayılan güncelleme türüne sahip kategoriler içeriyorsa, bu kategoriler güncellendiğinde katalog el ile güncellenmelidir. Katalog, **Dinamik** varsayılan güncelleme türüne sahip ürün kategorileri içeriyorsa, katalog her değiştiğinde otomatik olarak güncellenir.


<a name="see-also"></a>Ayrıca bkz.
--------

[Tedarik kategori hiyerarşisi ayarlama (Görev kılavuzu)](tasks/set-up-procurement-category-hierarchy.md)




