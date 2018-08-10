--- 
title: "Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme"
description: "Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a2b8534231c5fa50b1e0f709e09d318bb8202a43
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir. Bu kılavuzu çalıştırmadan önce bir taşıyıcı yakıt dizini ayarlamış olmanız gerekir. Bunu yapmak için "Taşıyıcı yakıt dizini kurma" kılavuzunu kullanabilirsiniz. Bu kurulum görevleri genellikle Lojistik Yöneticisi tarafından yapılır. Bu yöntemi oluşturmak için kullanılan demo verisi USMF'dir.


## <a name="create-an-accessorial-master"></a>Bir ana ilave oluştur
1. Taşıma yönetimi > Kurulum > Derecelendirme > Ana ilaveler öğesine gidin.
2. Yeni'ye tıklayın.
3. Ana ilaveler alanında bir değer girin.
4. İsim alanına bir değer yazın.
5. Kaydet'e tıklayın.

## <a name="create-a-carrier-accessorial-charge"></a>Taşıyıcı ilave masrafı oluşturun
1. Taşıma yönetimi > Kurulum > Derecelendirme > Taşıyıcı ilave masrafları öğesine gidin.
2. Yeni'ye tıklayın.
3. Taşıyıcı ilave numarası alanında bir değer girin.
4. Sevkiyat taşıyıcısı alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * Bu örnekte, Kamyon Taşıyıcısı'nı seçin.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Taşıyıcı hizmeti alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Ana ilaveler alanında, aramayı açmak için açılır menü düğmesine tıklayın.
10. Listede, istenen kaydı bulun ve seçin.
    * Bu örnekte, yeni oluşturulan Ana ilaveler'i seçin.  
11. Kaydet'e tıklayın.

## <a name="create-an-accessorial-assignment"></a>Bir ilave atama oluşturun
1. İlave atamaları'na tıklayın.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Ölçütler bölümünün genişletilmiş görünümüne geçin.
    * Kriterde, her zaman yakıt ek giderlerini uygulamayı veya bu örnek için sadece belirli bir bölge içerisinde uygulanacağını seçebilirsiniz.  
5. Posta kodu alanında bir değer girin.
6. Giden posta kodu alanında bir değer girin.
7. Hesaplama bölümünün genişletilmiş görünümüne geçin.
    * Hesaplama bölümünde yakıt ek giderlerini hesaplama yöntemini belirtebilirsiniz. Bu hesaplama, hesaplamanız için temel olarak seçtiğiniz ek birime bağlıdır.  
8. İlave ücret türü alanında 'Yakıt gideri' seçin.
9. İlave birim alanında 'Mesafe' seçin.
10. Bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, seçili satırdaki bağlantıya tıklayın.
12. Kaydet'e tıklayın.

## <a name="update-the-carrier-rating-profile"></a>Taşıyıcısı değerlendirme profilini güncelleyin
1. Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Değerlendirme profilleri bölümünün genişletilmiş görünümüne geçin.
4. Düzenle'yi tıklatın.
5. Taşıyıcı yakıt dizini alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Kaydet'e tıklayın.


