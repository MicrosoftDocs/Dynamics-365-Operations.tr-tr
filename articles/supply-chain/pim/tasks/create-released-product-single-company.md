---
title: Tek bir şirket için serbest bırakılan ürün oluşturma
description: Bu yordam, tek bir yasal birim bağlamında yayımlanan tek bir ürün oluşturmayı adım adım anlatılmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5306d41ab91213fdc7de0d3dd23d6845c5b8657
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147745"
---
# <a name="create-a-released-product-for-a-single-company"></a>Tek bir şirket için serbest bırakılan ürün oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, tek bir yasal birim bağlamında yayımlanan tek bir ürün oluşturmayı adım adım anlatılmaktadır. Yayımlanan ürün oluşturulduktan sonra, yalnızca bu birimde hemen kullanılabilir. Bu yordamı, USMF demo verisi şirketi aracılığıyla uygulayabilirsiniz. Bu görev, genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.


## <a name="create-a-released-product"></a>Serbest bırakılan ürün oluşturma
1. Serbest bırakılan ürünler öğesine gidin.
2. Yeni'ye tıklayın.
3. Ürün numarası alanında bir değer girin.
    * Ürün numarası, ürün numarası alanına otomatik olarak girilmezse, benzersiz bir ürün numarasını yazın. Bu adım yalnızca ürün numaraları için numara sırası ayarlanmadıysa gereklidir.  
4. Ürün adı alanına bir değer girin.
    * Ürün adı, arama adına varsayılan olarak alınır. Gerekirse, arama adını değiştirmeyi tercih edebilirsiniz.  
5. Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Bu madde modeli grupları, maddelerin madde girişlerinde ve çıkışlarında kontrol edilme ve işlenme biçimini belirleyen ayarları içerir. Bu ayarlar madde tüketiminin nasıl hesaplanacağını da belirler.  
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Stok maddelerini madde özelliklerini temel alan gruplara ayırarak stoku yönetmek için madde grupları kullanılır. Örneğin, bilgilerin ana hesaplara nasıl aktarıldığını yönetmek için bir dizi belirli ana hesap ile ilişkili farklı madde grupları oluşturabilirsiniz. Bu maddelerin stok değerini farklı aşamalarda izlemenize olanak sağlar.  
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Depolama stok boyutları maddelerin nasıl depolandığını ve stoktan alındığını kontrol etmenize yardım eder. Örneğin, bir depolama boyutu, tesis ve ambar olabilir.  
12. Listede, istenen kaydı bulun ve seçin.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * İzleme boyutu grubu hangi izleme boyutlarını bir ürüne atayabileceğinizi belirler. Örneğin, toplu iş numarası ve seri numarası, stok maddelerini izlemek için kullanılır.  
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. Stok birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Stok tutma birimi, ürünün stokta depolandığında miktarının nasıl ölçüleceğini belirler.  
18. Listede, istenen kaydı bulun ve seçin.
19. Listede, seçili satırdaki bağlantıya tıklayın.
20. Satınalma birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Satınalma birimi, ürünün bir satıcıdan satın alındığında miktar ölçümünün nasıl yapılacağını belirler.  
21. Listede, istenen kaydı bulun ve seçin.
22. Listede, seçili satırdaki bağlantıya tıklayın.
23. Satış birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Satış birimi, ürünün müşteriye satıldığında miktar ölçümünün nasıl yapılacağını belirler.  
24. Listede, istenen kaydı bulun ve seçin.
25. Listede, seçili satırdaki bağlantıya tıklayın.
26. Ürün reçetesi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Ürün reçetesi birimi (BOM), ürün reçetesi de dahil olmak üzere, ürünün nasıl ölçüleceğini belirler.  
27. Listede, istenen kaydı bulun ve seçin.
28. Listede, seçili satırdaki bağlantıya tıklayın.
29. Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Satış vergi grubundaki madde satış vergisi grubu, satış vergisinin her bir madde için nasıl hesaplandığını belirler.  
30. Listede, istenen kaydı bulun ve seçin.
31. Listede, seçili satırdaki bağlantıya tıklayın.
32. Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Satınalma vergilendirmesi grubundaki madde satış vergisi grubu, satınalma vergisinin her bir madde için nasıl hesaplandığını belirler.  
33. Listede, istenen kaydı bulun ve seçin.
34. Listede, seçili satırdaki bağlantıya tıklayın.
35. Tamam'a tıklayın.

## <a name="add-product-characteristics"></a>Ürün özellikleri ekleyin.
1. Stok yönetimi bölümünü genişletin veya daraltın.
2. Net ağırlık alanına bir sayı girin.
3. Dara alanına bir sayı girin.
4. Brüt derinlik alanına bir sayı girin.
5. Brüt genişlik alanına bir sayı girin.
6. Brüt yükselik alanına bir sayı girin.
7. Hacim alanına bir sayı girin.

## <a name="add-financial-dimensions"></a>Mali boyutlar ekleyin
1. Mali boyutlar bölümünü genişletin veya daraltın.
2. BusinessUnit alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. ItemGroup modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.
12. Listede, istenen kaydı bulun ve seçin.
13. Listede, seçili satırdaki bağlantıya tıklayın.

