--- 
title: "Tedarik kataloğu oluşturma"
description: "Bu kılavuzda bir tedarik kataloğunu nasıl oluşturacağınız gösterilir."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Tedarik kataloğu oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuzda bir tedarik kataloğunu nasıl oluşturacağınız gösterilir. Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir. Ayrıca talep oluşturduklarında çalışanların kataloğu nasıl kullanabileceğini öğreneceksiniz. Katalog oluşturmadan önce sisteminizde bir tedarik kategorisi hiyerarşisi olması gerekir. Hiyerarşi, dahil olan tüm ürünlerle birlikte yeni katalog tarafından devralınır. Bu kılavuzu tedarik kategorisinin kullanılabilir olduğu demo veri şirketi USMF'de ve prosedür adımlarında kullanılan örneklerde kullanabilirsiniz.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Tedarik kategorisi hiyerarşisinin var olduğundan emin olun
1. Tedarik ve kaynak > Tedarik kategorileri'ne gidin.
    * Tedarik kategorisi hiyerarşisi USMF demo veri şirketinde kullanılabilir ve ürünler Ofis makineleri/Bilgisayarlar kategorisine eklenmiştir. Bu prosedürü bir görev kılavuzu olarak çalıştırıyorsanız kategoride gezinmek istediğinizde kılavuzun kilidini açmanız gerekebilir. Bir hiyerarşi kullanılabilir değilse Yeni'ye tıklayarak oluşturun. Bu yalnızca bir defa yapılabilir.  
2. Sayfayı kapatın.

## <a name="create-a-catalog"></a>Katalog oluşturma
1. Tedarik ve kaynak atama > Kataloglar > Tedarik katalogları'na gidin.
2. Açılır iletişim kutusunu açmak için Yeni tedarik kataloğu'na tıklayın.
3. İsim alanına bir değer yazın.
4. Tamam'ı tıklatın.
5. Ağaçtan 'CORP PROCUREMENT CATEGORIES'i genişletin.
6. Ağaçtan, 'OFFICE MACHINES'i genişletin.
7. Ağaçtan 'Bilgisayarlar'ı seçin.
    * Tedarik kategorisindeki ürünler listede görüntülenir. Kategoriye bir ürün eklemek isterseniz bunu Tedarik kategorisi hiyerarşisi sayfasından veya Madde ayrıntıları sayfasından yapmanız gerekir.  
    * Varsayılan güncelleştirme türü, tedarik kategorisi hiyerarşisine eklenen yeni ürünlerin katalogda anında görünür olup olmayacaklarını belirler. Güncelleştirme türü Dinamik olarak ayarlanmışsa değişiklikler anında görünür. Güncelleştirme türü Statik ise yeni ürünler, yalnızca katalog yeniden yayınlandıktan sonra kataloğu kullanan kişilerce görüntülenebilir. Yayımla eylemi sayfanın en üstündeki Eylem Bölmesi'nden kullanılabilir. Ürünler tedarik kategorisi hiyerarşisinden kaldırılırsa Varsayılan güncelleştirme türü alanındaki değerden bağımsız olarak değişiklik hemen görünür.  
8. Listede, istenen kaydı bulun ve seçin.
9. Gizle'ye tıklayın.
10. Eylem Bölmesi'nde, Kategori gezinmesi'ne tıklayın.
11. Devre dışı bırak'a tıklayın.
12. Eylem Bölmesi'nde, Kategori gezinmesi'ne tıklayın.
13. Etkinleştir'i tıklatın.
14. Kataloğu etkinleştir'e tıklayın.
15. Sayfayı kapatın.

## <a name="make-the-catalog-visible"></a>Kataloğu görünür yapın
1. Tedarik ve kaynak atama > Ayarlar > İlkeler > Satınalma ilkeleri'ne tıklayın.
2. Tedarik İlkesi USMF'yi seçin.
    * Tüzel kişilik için kullanıcı profilinize bağlanan çalışanın profilinizdeki ürünleri sipariş etmesine izin veren satınalma ilkesini seçmeniz gerekir. USMF demo verilerinde Yönetici kullanıcı Julia Funderburk adlı çalışana bağlanır ve USMF'de varsayılan olarak ürünleri sipariş eder.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Yeni oluşturduğunuz kataloğu seçin.
5. Tamam'a tıklayın.
6. Sayfayı kapatın.
7. Sayfayı kapatın.

## <a name="use-the-catalog"></a>Kataloğu kullanın
1. Tedarik ve kaynak atama > Satınalma talepleri > Tüm satınalma talepleri'ne tıklayın.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Tamam'a tıklayın.
5. Ürünler ekle'ye tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
    * Ürünleri filtrelemek için soldaki kategori hiyerarşisini veya listenin en üstündeki filtreyi kullanabilirsiniz.  
7. Satırlara ekle'yi tıklatın.
8. Listede, istenen kaydı bulun ve seçin.
9. Satırlara ekle'yi tıklatın.
10. Tamam'a tıklayın.


