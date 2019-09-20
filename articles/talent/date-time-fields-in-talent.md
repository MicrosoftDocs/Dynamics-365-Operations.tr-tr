---
title: Microsoft Dynamics 365 for Talent'ta tarih ve saatle çalış
description: Microsoft Dynamics 365 for Talent'ta tarih ve saat alanları kullanırken ne beklendiğinizi anlayın. Dış kaynak Dynamics 365 for Talent veya Common Data Service konumunda tarih ve saat verileriyle etkileşim kurarken bekleyeceğiniz açıklık elde edin.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791236"
---
# <a name="date-and-time-fields-in-talent"></a>Talent'taki Tarih ve Saat alanları

[!include [banner](includes/banner.md)]

**Tarih ve saat** alanları Dynamics 365 for Talent içinde temel bir kavramdır. Bir Dynamics 365 formu, Common Data Service ve dış kaynakta **tarih ve saat** verileriyle nasıl çalışacağının anlaşılması önemlidir.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Tarih ile Tarih ve saat alanı veri türleri arasındaki farkı anlama

**Tarih ve saat** alanları saat dilimi bilgilerini içerir, **Tarih** alanları ise içermez. **Tarih** alanları aynı bilgileri herhangi bir konumda görüntüler. **Tarih** alanına bir tarih girdiğinizde, Yetenek, bu tarihi de veritabanına yazar.

Bir **tarih ve saat** alanındaki verileri görüntülerken, ilk olarak tarih ve saat, **Kullanıcı seçenekleri** formunda (**Ortak > Kurulum > Kullanıcı seçenekleri**) ayarlanan saat dilimine göre ayarlanır. Alana girdiğiniz tarih ve saat bilgileri veritabanına yazılan bilgilerle aynı olmayabilir.

[![Kullanıcı seçenekleri formu](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Formlardaki Tarih ve Saat alanlarını anlama 

**Tarih ve saat** alanına veri girerken, kullanıcının saat dilimi Eşgüdümlü Evrensel Saat'e (UTC) ayarlanmamışsa, ekranda görüntülenen veriler veritabanında depolanan verilerle aynı değildir. **Tarih ve saat** alanlarındaki veriler her zaman UTC olarak depolanır.

[![Çalışan formu](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Veritabanında Tarih ve Saat alanlarını anlama 

Yetenek **Tarih ve saat** değerini veritabanına yazdığında verileri UTC'de depolar. Bu, kullanıcıların Kullanıcı seçeneklerinde tanımlanan saat dilimine göre herhangi bir **tarih ve saat** verisini görmesini sağlar.
 
Yukarıdaki örnekte başlangıç zamanı zamanda bir noktadır, belirli bir tarihi değil. Oturum açmış olan kullanıcının saat dilimini GMT + 12:00'den GMT UTC'ye değiştirerek, yeni oluşturulan kayıt 01/05/2019 12:00:00 yerine 30/04/2019 12:00:00 gösterir.
  
Aşağıdaki örnekte, çalışan 000724 istihdamı saat diliminden bağımsız olarak aynı anda etkin olur. Çalışan GMT saat diliminde 30/04/2019 tarihinde etkin olacak ve GMT + 12:00 saat dilimindeki 05/01/2019 ile aynıdır. Her ikisi de belirli bir tarih değil, zaman içinde aynı noktaya başvuruda bulunuyor. 

[![Çalışan formu](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Veri yönetimi çerçevesi, Excel, Common Data Service ve Power BI'da Tarih ve Saat verileri 

Veri yönetimi çerçevesi, Excel eklentisi, Common Data Service ve Power BI raporlama, verilerle doğrudan veritabanı düzeyinde etkileşimde bulunmak üzere tasarlanmıştır. **Tarih ve saat** verilerini kullanıcının saat dilimine göre ayarlayabileceği bir istemci olmadığından, tüm **tarih ve saat** değerleri UTC'de olup verileri girerken veya görüntülerken bazı yanlış varsayımlar sağlar.  
 
DMF, Excel veya Common Data Service ile gönderilen **tarih ve saat** verilerinin veritabanı tarafından UTC'de olduğu varsayılır. Verileri görüntüleyen kullanıcının kullanıcı saat dilimi UTC olarak ayarlanmadığından, bu durum, gönderilen **tarih ve saat** değerinin beklendiği gibi görüntülenmediği durumlarda bazı karışıklıklara neden olabilir. 
 
Veriler dışa aktarıldığında aynı şey ters yönde de gerçekleşebilir. Dışa aktarılan DMF varlığındaki **tarih ve saat** verileri farklı olabilir ve böylece Dynamics istemcisinde görüntülenir. 
 
Verileri görüntülemek veya yazmak için DMF gibi harici kaynaklar kullanırken, kullanıcının bilgisayarının saat dilimi veya geçerli kullanıcı zaman dilimi ayarları ne olursa olsun, **Tarih ve Saat** değerlerinin UTC'de varsayılan olarak değerlendirildiğine dikkat edin. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Farklı ürün alanlarında görüntülenen aynı kayda örnekler 

**Kullanıcı saat dilimi UTC olarak ayarlanan Yetenek**

[![Çalışan formu](./media/worker-form3.png)](./media/worker-form3.png)

**Kullanıcı saat dilimi GMT +12:00 olarak ayarlanan Yetenek** 

[![Çalışan formu](./media/worker-form4.png)](./media/worker-form4.png)

**OData aracılığıyla Excel**

[![OData aracılığıyla Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF Aşamalandırma**

[![DMF Aşamalandırma](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF dışa aktarma**

[![DMF Aşamalandırma](./media/DMFexport.png)](./media/DMFexport.png)

**Common Data Service İle Excel**

[![Common Data Service İle Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>Ayrıca bkz.

[Tarih ve saat verileri](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kullanıcının tercih ettiği saat dilimleri](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
