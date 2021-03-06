---
title: Tarih ve Saat alanlarını anla
description: Microsoft Dynamics 365 Human Resources'ta tarih ve saat alanları kullanırken ne beklendiğinizi anlayın.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e5726f7e4beea1584b9a8e142212531ba1db56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051749"
---
# <a name="understand-date-and-time-fields"></a>Tarih ve Saat alanlarını anlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Tarih ve saat** alanları Dynamics 365 Human Resources içinde temel bir kavramdır. Formlar, Dataverse ve dış kaynaklardaki **Tarih ve Saat** verileriyle nasıl çalışılacağını anlamak önemlidir.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Tarih ile Tarih ve saat alanı veri türleri arasındaki farkı anlama

**Tarih ve saat** alanları saat dilimi bilgilerini içerir, **Tarih** alanları ise içermez. **Tarih** alanları aynı bilgileri herhangi bir konumda görüntüler. **Tarih** alanına bir tarih girdiğinizde, İnsan Kaynakları, bu tarihi de veritabanına yazar.

Bir **tarih ve saat** alanındaki verileri görüntülerken, İnsan Kaynakları tarih ve saat, **Kullanıcı seçenekleri** formunda (**Ortak > Kurulum > Kullanıcı seçenekleri**) ayarlanan saat dilimine göre ayarlar. Alana girdiğiniz tarih ve saat bilgileri veritabanına yazılan bilgilerle aynı olmayabilir.

[![Kullanıcı seçenekleri formu](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Formlardaki Tarih ve Saat alanlarını anlama 

Kullanıcının saat dilimi Eşgüdümlü Evrensel Saat (UTC) olarak ayarlanmazsa ekranda görüntülenen **Tarih ve Saat** verileri veritabanında depolanan verilerle aynı değildir. **Tarih ve saat** alanlarındaki veriler her zaman UTC olarak depolanır.

[![Çalışan formu UTC](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Veritabanında Tarih ve Saat alanlarını anlama 

Human Resources veritabanına bir **Tarih ve Saat** değeri yazdığında, verileri UTC'ye göre depolar. Bu, kullanıcıların Kullanıcı seçeneklerinde tanımlanan saat dilimine göre herhangi bir **tarih ve saat** verisini görmesini sağlar.
 
Yukarıdaki örnekte başlangıç zamanı zamanda bir noktadır, belirli bir tarihi değil. Oturum açan kullanıcının saat dilimi GMT +12:00'den GMT UTC'ye değiştirildiğinde aynı kayıt 01/05/2019 12:00:00 yerine 30/04/2019 12:00:00'yi gösterir.
  
Aşağıdaki örnekte, çalışan 000724 istihdamı saat diliminden bağımsız olarak aynı anda etkin olur. Çalışan GMT saat diliminde 30/04/2019 tarihinde etkin olacak ve GMT + 12:00 saat dilimindeki 05/01/2019 ile aynıdır. Her ikisi de belirli bir tarih değil, zaman içinde aynı noktaya başvuruda bulunuyor. 

[![Çalışan formu GMT](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Veri yönetimi çerçevesi, Excel, Dataverse ve Power BI'da Tarih ve Saat verileri 

Veri yönetimi çerçevesi, Excel eklentisi, Dataverse ve Power BI raporlama, verilerle doğrudan veritabanı düzeyinde etkileşimde bulunmak üzere tasarlanmıştır. **Tarih ve Saat** verilerini kullanıcının saat dilimine ayarlayan bir istemci olmadığından, tüm **Tarih ve Saat** değerleri UTC'ye göredir ve bu da veri girerken veya görüntülerken bazı yanlış varsayımlara yol açabilir.  
 
DMF, Excel veya Dataverse aracılığıyla gönderilen **Tarih ve Saat** verilerinin veritabanı tarafından UTC'ye göre olduğu varsayılır. Verileri görüntüleyen kullanıcının kullanıcı saat dilimi UTC olarak ayarlanmadığından, bu durum, gönderilen **tarih ve saat** değerinin beklendiği gibi görüntülenmediği durumlarda bazı karışıklıklara neden olabilir. 
 
Veriler dışa aktarıldığında aynı şey ters yönde de gerçekleşebilir. Dışarı aktarılan DMF varlığındaki **Tarih ve Saat** verileri Dynamics istemcisinde görüntülenenden farklı olabilir. 
 
Verileri görüntülemek veya yazmak için DMF gibi dış kaynakları kullanırken, **Tarih ve Saat** değerlerinin, kullanıcının bilgisayarının saat dilimine veya geçerli kullanıcı saat dilimi ayarlarına bakılmaksızın varsayılan olarak UTC'ye göre olduğunun kabul edildiğini unutmayın. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Farklı ürün alanlarında görüntülenen aynı kayda örnekler 

**Kullanıcı saat dilimi UTC olarak ayarlanan İnsan Kaynakları**

[![Çalışan formu UTC olarak ayarlandı](./media/worker-form3.png)](./media/worker-form3.png)

**Kullanıcı saat dilimi GMT+12:00 olarak ayarlanan İnsan Kaynakları** 

[![Çalışan formu GMT olarak ayarlandı](./media/worker-form4.png)](./media/worker-form4.png)

**OData aracılığıyla Excel**

[![OData aracılığıyla Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF Aşamalandırma**

[![DMF Aşamalandırma](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF dışa aktarma**

[![DMF Dışarı Aktarma](./media/DMFexport.png)](./media/DMFexport.png)

**Dataverse İle Excel**

[![Dataverse İle Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Ayrıca bkz.

[Tarih ve saat verileri](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kullanıcının tercih ettiği saat dilimleri](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]