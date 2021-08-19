---
title: Serbest metin fatura şablonu oluşturma
description: Bu prosedürde, serbest metin faturası şablonunun nasıl oluşturulduğu gösterilmektedir.
author: ShivamPandey-msft
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f84345aa8b157c5ca2a3025d4817af1fb1b1b2d009b3213d15a5b3daca8d763
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763274"
---
# <a name="create-a-free-text-invoice-template"></a>Serbest metin fatura şablonu oluşturma

[!include [banner](../includes/banner.md)]

Bu örnek için USMF demo şirketini kullanın. Bu prosedür, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.

## <a name="create-a-template"></a>Şablon oluştur

1. Alacak hesapları > Faturalar > Yinelenen faturalar > Serbest metin faturası şablonları'na gidin.
    * Fatura satırlarını, masrafları, bir muhasebe dağılım şablonu ve genel muhasebe hesabı bilgilerini içerebilen serbest metin faturası şablonları oluşturmak için bu formu kullanın.  
2. Yeni bir serbest metin faturası şablonu oluşturmak için "Yeni"ye tıklayın.
3. Şablon adı alanına bir değer girin.
    * "Şablon adı" serbest metin faturası şablonunu benzersiz olarak tanımlar. İki şablon aynı "Şablon adı"nı taşıyamaz.  
4. Açıklama alanına şablon grubu için bir açıklama girin.
5. Fatura satırları sekmesini genişletin.
6. Açıklama alanına, fatura satırı için bir açıklama girin.
7. Ana hesap alanında bir gelir hesabı seçin.
    * Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.  
8. Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.  
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Madde vergisi grubu alanında, geçerli fatura satırının madde satış vergisi grubunu seçin.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Birim fiyatı alanında, fatura satırının birim başına fiyatını girin veya görüntüleyin.
    * Bu tutar, fatura satırı tutarını belirlemek için, Miktar alanındaki değerle çarpılır.  
13. Serbest metin faturası şablonuna yeni satır ekleyin.
14. Açıklama alanına, fatura satırı için bir açıklama girin.
15. Ana hesap alanında bir gelir hesabı seçin.
    * Toplam fatura tutarı için müşteri alacağının mahsup hareket hesabını Müşteri deftere nakil profilleri sayfasında seçebilirsiniz.  
16. Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Geçerli fatura satırı için satış vergisi grubu, müşteri hesabının satış vergisi grubu varsayılan değeridir.  
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Geçerli fatura satırı için madde satış vergisi grubu.  
19. Listede, seçili satırdaki bağlantıya tıklayın.
20. Fatura satırı için birim sayısını girin veya görüntüleyin
    * Bu sayı, fatura satırı tutarını belirlemek için, Birim fiyatı alanındaki değerle çarpılır.  
21. Fatura satırı için birim başına fiyatı girin veya görüntüleyin. 
    * Bu tutar, fatura satır tutarını belirlemek için, Miktar alanındaki değerle çarpılır.  
22. Tek bir satır ve tüm alt satırları için muhasebe dağılımlarını görüntüleyin veya değiştirin.
    * Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlar.  
23. Seçili fatura satırı için muhasebe dağılımlarını güncelleştirin.
24. Kapat’a tıklayın.

## <a name="save-a-free-text-invoice-as-a-template"></a>Bir serbest metin faturasını şablon olarak kaydetme
Mevcut bir serbest metin faturasını şablon olarak da kaydedebilirsiniz. Fatura sekmesinden "Şablona kaydet"i seçtiğiniz zaman şablon için bir ad ve açıklama girin. Aynı adı taşıyan bir şablon varsa, bu adda bir şablonun zaten var olduğuna ilişkin bir bildirim görürsünüz. Yine de, Tamam'a tıklayarak şablonun yerine yenisini geçirebilirsiniz. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]