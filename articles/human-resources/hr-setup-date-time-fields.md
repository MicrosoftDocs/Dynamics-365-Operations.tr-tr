---
title: Tarih ve Saat alanlarını anlama
description: Bu konu, Microsoft Dynamics 365 Human Resources'ta tarih ve saat alanlarının nasıl kullanılacağını açıklar.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f595e06d9ddc9b44e8820d814d888971444bdf6a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688503"
---
# <a name="understand-date-and-time-fields"></a>Tarih ve Saat alanlarını anlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Tarih ve saat** alanları, Microsoft Dynamics 365 Human Resources içinde temel bir kavramdır. Sayfalar, Dataverse ve dış kaynaklardaki **Tarih ve Saat** verileriyle nasıl çalışılacağını anlamak önemlidir.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Tarih ile Tarih ve saat alanı veri türleri arasındaki farkı anlama

**Tarih ve saat** alanları saat dilimi bilgilerini içerir, **Tarih** alanları ise içermez. **Tarih** alanları aynı bilgileri herhangi bir konumda gösterir. **Tarih** alanına bir tarih girdiğinizde, bu tarih de veritabanına yazılır.

Bir **Tarih ve Saat** alanındaki verileri görüntülerken, **Kullanıcı Seçenekleri** sayfasında (**Ortak \> Kurulum \> Kullanıcı seçenekleri**) ayarlanan saat dilimine göre ayarlanır. Alana girdiğiniz tarih ve saat bilgileri, veritabanına yazılan bilgilerle aynı olmayabilir.

[![Kullanıcı seçenekleri sayfası.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Sayfalardaki Tarih ve Saat alanlarını anlama 

Kullanıcının saat dilimi Eşgüdümlü Evrensel Saat (UTC) olarak ayarlanmazsa ekranda görüntülenen **Tarih ve Saat** verileri veritabanında depolanan verilerle aynı değildir. **Tarih ve saat** alanlarındaki veriler her zaman UTC olarak depolanır.

[![Çalışan sayfa UTC'si.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Veritabanında Tarih ve Saat alanlarını anlama 

**Tarih ve saat** değeri veritabanına yazıldığında, veriler UTC olarak depolanır. Bu nedenle, kullanıcılar kullanıcı seçeneklerinde tanımlanan saat dilimine göre herhangi bir **Tarih ve Saat** verilerini görebilir.
 
Yukarıdaki örnekte başlangıç zamanı zamanda bir noktadır, belirli bir tarihi değil. Oturum açan kullanıcının saat dilimi GMT +12:00'den GMT UTC'ye değiştirildiğinde aynı kayıt 01/05/2019 12:00:00 yerine 30/04/2019 12:00:00'yi gösterir.

Aşağıdaki örnekte, çalışan 000724 istihdamı saat diliminden bağımsız olarak aynı anda etkin olur. Çalışan GMT saat diliminde 30/04/2019 tarihinde etkin olacak ve GMT + 12:00 saat dilimindeki 05/01/2019 ile aynıdır. Her ikisi de belirli bir tarih değil, zaman içinde aynı noktaya başvuruda bulunuyor. 

[![Çalışan sayfa GMT'si.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Veri yönetimi çerçevesi, Excel, Dataverse ve Power BI'da Tarih ve Saat verileri 

Veri Yönetimi Çerçevesi (DMF), Excel eklentisi, Dataverse ve Power BI raporlama, verilerle doğrudan veritabanı düzeyinde etkileşimde bulunmak üzere tasarlanmıştır. **Tarih ve Saat** verilerini kullanıcının saat dilimine ayarlayan bir istemci olmadığından, tüm **Tarih ve Saat** değerleri UTC'ye göredir ve bu da veri girerken veya görüntülerken bazı yanlış varsayımlara yol açabilir.
 
DMF, Excel veya Dataverse ile gönderilen **Tarih ve Saat** verilerinin veritabanı tarafından UTC'de olduğu varsayılır. Ancak, verileri görüntüleyen kullanıcıların kullanıcı saat dilimi UTC'ye ayarlı değilse, gönderilen **Tarih ve Saat** değeri beklendiği gibi görünmez ve kullanıcıların kafası karışabilir. 
 
Veriler dışa aktarıldığında aynı şey ters yönde de gerçekleşebilir. Dışarı aktarılan DMF varlığındaki **Tarih ve Saat** verileri Dynamics istemcisinde görüntülenenden farklı olabilir. 
 
Verileri görüntülemek veya yazmak için DMF gibi dış kaynakları kullanırken, **Tarih ve Saat** değerlerinin, kullanıcının bilgisayarının saat dilimine veya geçerli kullanıcı saat dilimi ayarlarına bakılmaksızın varsayılan olarak UTC'ye göre olduğunun kabul edildiğini unutmayın. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Farklı ürün alanlarında görüntülenen aynı kayda örnekler 

**Kullanıcı saat dilimi UTC olarak ayarlanan İnsan Kaynakları**

[![Çalışan sayfası UTC olarak ayarlandı.](./media/worker-form3.png)](./media/worker-form3.png)

**Kullanıcı saat dilimi GMT+12:00 olarak ayarlanan İnsan Kaynakları** 

[![Çalışan sayfası GMT olarak ayarlandı.](./media/worker-form4.png)](./media/worker-form4.png)

**OData aracılığıyla Excel**

[![OData aracılığıyla Excel.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF Aşamalandırma**

[![DMF Aşamalandırma.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF dışa aktarma**

[![DMF Dışarı aktarma.](./media/DMFExport.png)](./media/DMFExport.png)

**Dataverse İle Excel**

[![ Dataverse üzerinden Excel.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Ayrıca bkz.

[Tarih ve saat verileri](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kullanıcının tercih ettiği saat dilimleri](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
