---
title: İş belgesi şablonunun yapısını güncelleme
description: Bu makalede, İş belgesi yönetimi özelliği kullanılarak iş belgesi şablonunun yapısının nasıl güncelleştirileceği açıklanmaktadır.
author: kfend
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
ms.openlocfilehash: 793f327a3e5861e03b6ae67da8149f1db11e47bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285530"
---
# <a name="update-the-structure-of-a-business-document-template"></a>İş belgesi şablonunun yapısını güncelleştirme 

[!include[banner](../includes/banner.md)]

[İş belgesi yönetimi](er-business-document-management.md) şablon düzenleyicisinin **Şablon yapısı** bölmesinde, Microsoft Excel'de bir şablona [yeni alanlar ekleyerek](er-bdm-add-field-to-excel-template.md) iş belgesi şablonunu değiştirebilirsiniz. Ardından şablonun yapısı, Dynamics 365 Finance'te **Şablon yapısı** bölmesinde yaptığınız değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilir.

Ayrıca, şablonu Office 365 çevrimiçi işlevini kullanarak da değiştirebilirsiniz. Örneğin, düzenlenebilir çalışma sayfasına resim veya şekil gibi yeni bir adlandırılmış öğe ekleyebilirsiniz. Bu durumda, şablonun yapısı Finance'te otomatik olarak güncelleştirilmez ve eklediğiniz öğe **Şablon yapısı** bölmesinde gösterilmez. Şablon düzenleyicisi sayfasında **Yapıyı güncelleştir**'i seçerek Finance'teki şablon yapısını el ile güncelleştirin.

Bu özellik hakkında daha fazla bilgi için aşağıdaki örneği tamamlayın.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Örnek: İş belgesi şablonunun yapısını güncelleştirme

Bu örnekte, şablon Office Online'da değiştirildikten sonra sistem yöneticisinin iş belgesi şablonunun yapısını nasıl güncelleştirebileceği gösterilmektedir. Aşağıdaki bölümlerde ilgili adımlar açıklanmaktadır.

### <a name="prepare-a-business-document-template-for-editing"></a>Düzenleme için bir iş belgesi şablonu hazırlama

[İş belgesi yönetimine genel bakış](er-business-document-management.md)'ta aşağıdaki yordamları tamamlayın.

1. [ER parametrelerini yapılandırma](er-business-document-management.md#configure-er-parameters)
2. [ER çözümlerini çe aktar](er-business-document-management.md#import-er-solutions)
3. [İş belgesi yönetimini etkinleştirme](er-business-document-management.md#enable-business-document-management)
4. [Parametrelerini yapılandırma](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>İş belgesi şablonu düzenleme

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.
2. **Yeni şablon oluştur** sayfasında, **Serbest metin faturası (ER örneği) (Excel)** şablonunu seçin.
3. **Belge oluştur**'u seçin.
4. **Başlık** alanına **FTI sample Litware** başlığını girin.
5. Yeni şablonu oluşturmak için **Tamam**'ı seçin.

    > [!NOTE]
    > Henüz Office Online'da oturum açmadıysanız [Office 365 oturum açma sayfasına yönlendirilirsiniz](er-business-document-management.md#frequently-asked-questions). Finance ortamınıza dönmek için tarayıcınızda **Geri** düğmesini seçin.

    Yeni şablon, şablon düzenleyicisi sayfasındaki Excel Online eklenmiş denetiminde düzenlenmek üzere açılır.

[![İş belgesi şablonunu düzenlemeye başlamak için İş belgesi yönetimi çalışma alanını kullanma.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Düzenlenebilir şablonun geçerli yapısını inceleme

1. Excel Online'daki şeritte, **Görünüm** sekmesinde, **Göster** grubunda **Kılavuz çizgileri**'ni seçin.
2. Düzenlenebilir şablonda, şablon başlığının üstündeki dikdörtgeni seçin. Bu dikdörtgen, **rptHeaderCompLogo** adlı bir resimdir.
3. **Şablon yapısı** bölmesi gizliyse **Yapıyı göster**'i seçin.
4. **Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.
5. Finance'teki şablon yapısında **rptHeaderCompLogo** öğesnini, **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesinin alt öğesi olarak sunulduğuna dikkat edin.

[![Düzenlenebilir şablonun geçerli yapısını incelemek için İş belgesi yönetimi çalışma alanını kullanma.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Bir resim silerek iş belgesi şablonunun yapısını güncelleştirme

1. Excel Online'da, düzenlenebilir şablonda, **rptheadercomplogo** resmini seçin.
2. Seçili resmi düzenlenebilir şablondan silmek için aşağıdaki adımlardan birini izleyin:

    - Klavyenizde **Delete** tuşunu seçin.
    - Resmi seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Kes**'i seçin.

    > [!NOTE]
    > Bu durumda, **rptHeaderCompLogo** öğesi Finance'teki şablon yapısında bulunmaya devam etse de artık Excel şablosunda yer almaz.

3. Excel ve Finance'teki şablon yapısını eşitlemek **Yapıyı güncelleştir**'i seçin.
4. **Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.
5. **rptHeaderCompLogo** öğesinin, artık Finance'teki şablon yapısında yer almadığını görebilirsiniz.

[![İş belgesi şablonundan bir resim silmek için İş belgesi yönetimi çalışma alanını kullanma.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Bir resim ekleyerek iş belgesi şablonunun yapısını güncelleştirme

1. Excel Online'daki şeritte, **Ekle** sekmesinde, **Çizimler** grubunda **Resim**'i seçin.
2. **Dosya seç**'i belirleyin, eklemek istediğiniz resme göz atın, resmi seçin ve ardından **Tamam**'ı seçin.
3. **Ekle**'yi seçin.
4. Yeni resmi doğru yere gelene kadar taşıyın. Varsayılan olarak, Excel resmi adlandırır. Örneğin, resim **Resim 2** olarak adlandırılabilir.
5. Excel ve Finance'teki şablon yapısını eşitlemek **Yapıyı güncelleştir**'i seçin.
6. **Şablon yapısı** bölmesinde **Rapor \> Fatura \> rptHeader \> rptHeaderPart1** öğesini genişletin.
7. Yeni resimin, artık Finance'teki şablon yapısında öğe olarak yer aldığını görebilirsiniz.

[![İş belgesi şablonuna resim eklemek için İş belgesi yönetimi çalışma alanını kullanma.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>İlgili bağlantılar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[İş belgesi yönetimine genel bakış](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
