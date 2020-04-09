---
title: RCS'de kullanılacak uygulama meta verileri hazırlama
description: Bu konudaki adımlarda, bir kullanıcının Regulatory Configuration Service'ta (RCS) ER model eşleme yapılandırmaları tasarlamaya yönelik uygulama meta verilerini içeren yeni Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d091cd835cfcb7164f83259b69e3bc1d7c09dc4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143166"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>RCS'de kullanılacak uygulama meta verileri hazırlama
[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlarda Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının Regulatory Configuration Service'ta (RCS) ER model eşleme yapılandırmaları tasarlamaya yönelik uygulama meta verilerini içeren yeni Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmaktadır. Bu yapılandırma dış ticaret işlemlerine erişmek için örnek bir ER modeli eşlemesi yapılandırması tasarlamak için kullanılacaktır. Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). adımlarını tamamlamanız gerekir.

## <a name="prerequisites"></a>Önkoşullar
1.    **Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin. 
2.    Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın. 
3.    **Meta veri yapılandırması**'na tıklayın. 
4.    Örnepin, dış ticari işletme etki alanındaki bilgileri içeren elektronik belgeler oluşturmak amacıyla kullanılacak Finance and Operations uygulamasına bir ER çözümü tasarlamak için RCS'yi kullanmak istiyorsunuz. ER veri modeliyle gerekli verilerin kaynakları arasındaki eşlemeyi belirtmek amacıyla RCS'de Finance and Operations uygulaması için uygulama meta verilerine erişiminizin olması gerekir. Bu nedenle, ER çözümünü tasarlama sürecinin bir parçası olarak, seçilen iş etki alanı için ER raporları oluşturmak üzere gerekli olan tüm meta verileri içeren yeni bir ER meta veri yapılandırması yapılandırıyoruz. 

## <a name="add-metadata-configuration"></a>Meta veri yapılandırması ekleme 
1.    İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın. 
2.    **Ad** alanına, "Dış ticaret meta verisi" yazın. 
3.    **Konfigürasyon oluştur**'u tıklatın. 
4.    **Tasarımcı**'yı tıklatın. 
5.    **Ekle** öğesine tıklayın. 
  
> [!NOTE]
> Tüm uygulama, seçili model ya da modüller için tüm meta verileri seçebilirsiniz. Bu durumda aşağıdaki meta verilerin otomatik olarak eklenebileceğine dikkat edin: kayıt tabloları, numaralandırmalar ve genişletilmiş veri türleri. Ek meta veri türleri gerektiğinde, bunların el ile eklenmesi gerekir. 
 
El ile seçmeniz gereken dış ticari hareketlerle ilgili bazı meta verilerimiz ve meta veri öğelerimiz var. 
  
6.    **Veri kaynağı ekle**'ye tıklayın. 
7.    **Tablo kayıtları**'na tıklayın. 
8.    **Ad** alanında bir "İntrastat" değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın. 
9.    **Intrastat** tablosu kaydını seçin. 
10.    **Tamam**'a tıklayın.
  
Intrastat kayıt tablosu hakkında meta veri bilgileri ekledik. 
  
11.    Ağaçta **Tablo kayıtları Instrastat**\>**İlişkiler**'i genişletin. 
12.    Ağaçta **Tablo kayıtları İntrastatı**\>**İlişkiler\IntrastatCommodity (Tablo kayıtları EcoResCategory)**'i seçin.     
13.    **Meta veri ekle**'yi seçin. 
  
> [!NOTE]
> Seçili kayıt tablosu için gerekli ilişkilerindeki meta veriler el ile eklenmelidir. 
  
16.    **Veri kaynağı ekle**'ye tıklayın. 
17.    **Numaralandırma**'yı seçin. 
18.    **Ad** alanında bir "IntrastatDirection" değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın. 
19.    **IntrastatDirection numaralandırma** kaydını seçin. 
20.    **Tamam**'a tıklayın. 
21.    **Kaydet**'e tıklayın.  
22.    Sayfayı kapatın. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Meta veri yapılandırmasının taslak sürümünü tamamlama
1.    **Durumu değiştir** öğesine tıklayın. 
2.    **Tamamla** öğesine tıklayın. 
3.    **Tamam**'a tıklayın. 
4.    Tamamlanmış sürüm **1**'i seçin. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Meta veri yapılandırmasının tamamlanan sürümünü uygulamadan XML dosyası olarak dışarı aktarın:
1.    **Değiştir**'e tıklayın. 
2.    **XML dosyası olarak dışa aktar**'a tıklayın. 
3.    **Tamam**'a tıklayın. 
    
Oluşturulan ER meta veri yapılandırması, RCS'ye alınabilecek ve dış ticari işletme etki alanının meta verileri hakkında bilgi kaynağı olarak kullanılabilen bir XML dosyası olarak kaydedildi. Bu bilgiye dayanarak uygulama meta verileri ve ER veri modeli arasındaki eşlemeyi belirtebiliriz.
