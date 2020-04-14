---
title: Tedarik kataloğu oluşturma
description: Bu konu tedarik kataloğunun nasıl oluşturulacağını açıklar.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94d5c3f6677ec10ea1b9ac3c488c3b8d7dc6856f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147492"
---
# <a name="create-a-procurement-catalog"></a>Tedarik kataloğu oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu tedarik kataloğunun nasıl oluşturulacağını açıklar. Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir. Ayrıca talep oluşturduklarında çalışanların kataloğu nasıl kullanabileceğini öğreneceksiniz. Katalog oluşturmadan önce sisteminizde bir tedarik kategorisi hiyerarşisi olması gerekir. Hiyerarşi, dahil olan tüm ürünlerle birlikte yeni katalog tarafından devralınır. Bu kılavuzu tedarik kategorisinin kullanılabilir olduğu demo veri şirketi USMF'de ve prosedür adımlarında kullanılan örneklerde kullanabilirsiniz.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Tedarik kategorisi hiyerarşisinin var olduğundan emin olun
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Tedarik kategorileri**'ne gidin. Tedarik kategorisi hiyerarşisi USMF demo veri şirketinde kullanılabilir ve ürünler **Ofis makineleri/Bilgisayarlar** kategorisine eklenmiştir. Bu prosedürü bir görev kılavuzu olarak çalıştırıyorsanız kategoride gezinmek istediğinizde kılavuzun kilidini açmanız gerekebilir. Bir hiyerarşi kullanılabilir değilse **Yeni**'ye tıklayarak oluşturun. Bu yalnızca bir defa yapılabilir.  
2. Sayfayı kapatın.

## <a name="create-a-catalog"></a>Katalog oluşturma
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Kataloglar > Tedarik katalogları**'na gidin.
2. Açılır iletişim kutusunu açmak için **Yeni tedarik kataloğu**'nu seçin.
3. **Ad** alanına bir değer yazın.
4. **Tamam**'ı seçin.
5. Ağaçtan **CORP PROCUREMENT CATEGORIES**'i genişletin.
6. Ağaçtan, **OFFICE MACHINES**'i genişletin.
7. Ağaçtan **Bilgisayarlar**'ı seçin.

  - Tedarik kategorisindeki ürünler listede görüntülenir. Kategoriye bir ürün eklemek isterseniz bunu **Tedarik kategorisi hiyerarşisi** sayfasından veya **Madde ayrıntıları** sayfasından yapmanız gerekir.  
  - **Varsayılan** güncelleştirme türü, tedarik kategorisi hiyerarşisine eklenen yeni ürünlerin katalogda anında görünür olup olmayacaklarını belirler. Güncelleştirme türü **Dinamik** olarak ayarlanmışsa değişiklikler anında görünür. Güncelleştirme türü **Statik** ise yeni ürünler, yalnızca katalog yeniden yayınlandıktan sonra kataloğu kullanan kişilerce görüntülenebilir. **Yayımla** eylemi sayfanın en üstündeki Eylem Bölmesi'nden kullanılabilir. Ürünler tedarik kategorisi hiyerarşisinden kaldırılırsa **Varsayılan** güncelleştirme türü alanındaki değerden bağımsız olarak değişiklik hemen görünür.  

8. Eylem bölmesinde **Kategori gezinmesi**'ni seçin ve **Etkin**'in seçili olduğundan emin olun.
9. **Kataloğı etkinleştir**'i seçin.
10. Sayfayı kapatın.

## <a name="make-the-catalog-visible"></a>Kataloğu görünür yapın
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Kurulum > İlkeler > Satın alma ilkeleri**'ne gidin.
2. **Tedarik İlkesi USMF**'yi seçin. Tüzel kişilik için kullanıcı profilinize bağlanan çalışanın profilinizdeki ürünleri sipariş etmesine izin veren satınalma ilkesini seçmeniz gerekir. USMF demo verilerinde Yönetici kullanıcı **Julia Funderburk** adlı çalışana bağlanır ve USMF'de varsayılan olarak ürünleri sipariş eder.  
3. Yeni oluşturduğunuz kataloğu seçin.
4. **Tamam**'ı seçin.

## <a name="use-the-catalog"></a>Kataloğu kullanın
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tüm satınalma talepleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir değer yazın.
4. **Tamam**'ı seçin.
5. **Ürün ekle**'yi seçin.
6. Listede, istenen kaydı bulun ve seçin. Ürünleri filtrelemek için soldaki kategori hiyerarşisini veya listenin en üstündeki filtreyi kullanabilirsiniz.  
7. **Satırlara ekle**'yi seçin.
8. **Tamam**'ı seçin.

