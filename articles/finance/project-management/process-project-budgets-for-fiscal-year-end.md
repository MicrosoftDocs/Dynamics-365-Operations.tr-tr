---
title: Proje bütçelerini mali yıl bitişinde transfer etme
description: Bu makalede, kalan Bütçe tutarlarının gelecekteki yıllara nasıl aktarılacağı ve bütçe kayıt ayrıntılarının nasıl oluşturulacağı hakkında bir bilgi verilir.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172342"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Proje bütçelerini mali yıl bitişinde transfer etme

[!include [banner](../includes/banner.md)]

Çok yıllık bir projede çalışırken, mali yılın sonunda bütçe kalan bütçesi olabilir. Kalan bütçe tutarlarını, gelecekteki bir yıla transfer edebilir ve ilgili genel muhasebe hesaplarındaki tutarlar için bütçe kaydı ayrıntılarını oluşturabilirsiniz. Kalan tutarları ileriye almadan önce kalan bütçe tutarlarını gözden geçirip analiz edin.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Kalan bütçe tutarlarını İncele ve analiz et

Projelere ait yıl sonu bütçe tutarlarını gözden geçirmek için aşağıdaki adımları tamamlayın, ancak tutarları ileriye doğru taşımaz.

1. **Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin. 
2. **Proje bütçesi taşıması ileriye doğru işlem** sayfasında, **yıl sonu seçenekleri** sekmesinde, **Kalan Proje Bütçe tutarlarını ilet** etkin olmadığını doğrulayın.
3. **Parametreler** sekmesinde, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin. 
4. **Mali yılı açma** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin. 
5. **İlk tahmin modeli** alanında, **kalan bütçeyi** seçin. 
6. Seçtiğiniz ölçütlere uyan ve kalan bütçeyi içermeyen projeleri dahil etmek için, **Kalan sıfır göster**'i seçin.  
7. **Bütçe Seç** sekmesinde, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin ve ardından **İşle**'yi seçin. 
8. Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçilen bütçeleri al**'ı seçin.

Bölmedeki belirli bir satırla ilgili daha fazla bilgi için, satırı seçin ve **Bütçe ayrıntılarını görüntüle** veya **Firmaları görüntüle**'yi seçin.

## <a name="carry-forward-remaining-budget-amounts"></a>Kalan bütçesi tutarlarını devret 

Kalan bütçe tutarlarını işleseniz, genel muhasebede, ilettiğiniz tutarlar için hareketler oluşturabilirsiniz. Genel muhasebe hareketleri oluşturmak için [bütçe tutarlarını ileriye taşı ve genel muhasebe hareketleri oluştur](#carry-forward) bölümdeki adımları tamamlayın. 

> [!NOTE]
> İleriye doğru gerçekleştirilen bütçe tutarları **tahmin modelleri** sayfasında, ileri sarma tahmin modeli olarak seçilen tahmin modeline transfer edilir.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Bütçe tutarlarını ileri sar ve genel muhasebe hareketleri oluştur

1.  **Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin. 
2. **Proje bütçesi devam ediyor-ileri işlem** sayfasında **yıl sonu** seçeneğini belirleyin ve sonra da **genel muhasebede kalan proje bütçe tutarlarını ileri sar** ve **bütçe kayıt girişleri oluştur** seçeneğini etkinleştirin. 
3. **Parametreler** sekmesinde, **proje parametreleri** alan grubunda aşağıdakileri seçin:

   - **Proje bütçe yılı**:Kalan bütçe tutarlarını görüntülemek istediğiniz mali yılı başını seçin. 
   - **Kar ve zarar**: Genel muhasebede kar ve zarar hareketleri oluşturun. 
   -  **Süren iş**: Süren İş (WIP) hareketlerini genel muhasebede oluşturun.
   -  **Bordro**: Genel muhasebede Bordro tahsisatı hareketleri oluşturun. 

5. **Genel muhasebe** alanı grubunda aşağıdaki bilgileri sağlayın: 

   - **Mali yılı açma** alanında, kalan bütçe tutarlarını aktarmak istediğiniz projeler için mali yılı seçin. Varsayılan değer, **proje bütçe yılı** alanındaki değerden sonraki bir yılla yapılır.
   -  **Hareket-ileri dönemi** alanında, genel muhasebede bütçe kaydı ayrıntılarını oluşturmak istediğiniz dönemi seçin. Bu, genellikle açılış mali yıldaki ilk dönemdir.

6. **Şuradan/Şuraya kopyala** alanı grubunda aşağıdaki bilgileri sağlayın:

   - **İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarıyla ilişkili proje bütçe tahmin modelini seçin. 
   - **Muhasebe bütçe modeline** alanında, genel muhasebeye aktarmak istediğiniz bütçe tutarlarıyla ilişkili öuhasebe bütçe tahmin modelini seçin. 
   -  Projelere ait bütçe tutarlarını transfer ettiğinizde oluşturulan genel muhasebe hareketleri için projenin satış para birimini kullanmak üzere **transfer satış para birimi**'ni seçin. Bu seçenek işaretli değilse, hareketler muhasebe para birimini kullanır. 
   -  Kalan bütçe tutarları olmayan projeleri dahil etmek için **Kalan sıfır göster**'i seçin, ancak alt bölmede görüntülenen projelerde seçtiğiniz diğer ölçütleri karşılayabilirsiniz.

7. **Bütçe Seç** sekmesinde, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin. Belirli bir proje bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak isterseniz, **Seçilen bütçeleri al**'ı seçin.
8. İşlemek istediğiniz her proje için, projenin satır başındaki seçeneği belirleyin.

    > [!TIP]
    > Projelerin tümünü veya bir çoğunu seçmek için, sol üst köşedeki onay işaretini seçin. Herhangi bir projenin işlenmesini hariç tutmak için projenin onay işaretini kaldırın.

9. Seçili projeler için kalan bütçe tutarlarını seçili mali yıla aktarmak ve genel muhasebede bütçe kayıt ayrıntıları oluşturmak için, **işlem** seçeneğini belirleyin.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Genel muhasebe hareketleri oluşturmadan bütçe tutarlarını ileri sar

1. **Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin.
2. **Proje bütçesi taşıması ileriye doğru işlem** sayfasında, **yıl sonu seçenekleri** alanında, **Kalan Proje Bütçe tutarlarını ilet**'i seçin.
3. **Parametreler** grubunda, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin.
4. **Şuradan/Şuraya kopyala** grubunda aşağıdaki bilgileri sağlayın:

   - **İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarıyla ilişkili proje bütçe tahmin modelini seçin. 
   - Seçtiğiniz ölçütlere uyan ve kalan bütçeyi içermeyen projeleri dahil etmek için, **Kalan sıfır göster**'i seçin.
   - **Bütçe Seç** grubunda, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin. Belirli bir proje bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçilen bütçeleri al**'ı seçin.

5. İşlemek istediğiniz her proje için, projenin satır başındaki seçeneği belirleyin. 
6. Seçili **projeler** için kalan Bütçe tutarlarının seçili mali yıla aktarılması işlemini seçin.

