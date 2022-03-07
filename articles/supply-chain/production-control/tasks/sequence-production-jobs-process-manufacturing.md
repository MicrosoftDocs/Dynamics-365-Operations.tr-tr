---
title: Süreç üretimi için üretim işlerini sıralama
description: Bu prosedürde, planlanan siparişlerin renk ve paket boyutu önceliğine göre nasıl sıralanacağının gösterilmesi için örnek olarak boya ürünleri kullanılmıştır.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e54cfa60fa9efd511aef8c074484b9b1a738e8cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572757"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Süreç üretimi için üretim işlerini sıralama

[!include [banner](../../includes/banner.md)]

Bu prosedürde, planlanan siparişlerin renk ve paket boyutu önceliğine göre nasıl sıralanacağının gösterilmesi için örnek olarak boya ürünleri kullanılmıştır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USPI'dir. Bu yordam için üretim planlayıcısına yöneliktir.


## <a name="run-master-planning-for-uspi"></a>USPI için master planlama yürüme
1. Master planlama > Master planlama > Çalıştır > Master planlama öğesine gidin.
2. Master plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * MasterPlan'ı seçin.  
4. Tamam'a tıklayın.
    * Bu işlem, sıralama işlemi dahil Master Planlamayı başlatır. Bu işlem birkaç dakika sürebilir.  

## <a name="view-planned-orders-for-the-paint-products"></a>Boya ürünleri için planlı siparişleri görüntüleme
1. Master planlama > Master planlama > Planlı siparişler öğesine gidin.
2. Madde ayrıntıları Hızlı Kutusunu genişletin.
3. Zamanlama ayrıntıları Hızlı Kutusunu genişletin.
4. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * MasterPlan'ı seçin.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Madde numarası alanında 'P300' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.
    * Sipariş tarihini ve teslimat tarihini görmek için sağa doğru kaydırarak kilidi açın. Bu maddelerin sipariş tarihinin Bugün olduğuna ve ürün adında da gösterildiği gibi, planlanan siparişler için teslim tarihlerinin, renk ve paket boyutu önceliğinden sonra sıralanmadığına dikkat edin. Ürün adını ve önceliğini görmek için bir madde numarasının üstüne gelin.  

## <a name="sequence-planned-orders-for-paint"></a>Boya için planlı siparişleri sıralama
1. Sayfayı kapatın.
2. Master planlama > Master planlama > Sıralanan planlı siparişler öğesine gidin.
3. Madde ayrıntıları Hızlı Kutusunu genişletin.
4. Zamanlama ayrıntıları Hızlı Kutusunu genişletin.
    * Not: Burada, planlı siparişler için Başlangıç tarihi/saatinin 28 günlük zaman aralığı dönemi içindeki renk ve paket boyutuna göre sıralandığını görüyorsunuz. Bu dönemler, Kampanya alanındaki bir sayıyla tanımlanır. Sıralı planlı sipariş formu, tipik bir planlı sipariş formu gibi hareket eder ve üretim planlayıcı, planlanan emirleri burada kesinleştirebilir.  
5. Tüm sıraları işaretleyin.
6. Kabul et düğmesini tıklatın.
    * Planlanan emirleri seçilen sıra eylemiyle Ertele veya Öne getir olarak günceller.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Planlı siparişlerin sırasını doğrulama
1. Sayfayı kapatın.
2. Master planlama > Master planlama > Planlı siparişler öğesine gidin.
3. Madde ayrıntıları Hızlı Kutusunu genişletin.
4. Zamanlama ayrıntıları Hızlı Kutusunu genişletin.
5. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
    * MasterPlan'ı seçin.  
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Madde numarası alanında 'P300' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.
    * Siparişlerin artık, renk ve boyut önceliğine göre sıralanacağına ve planlı siparişlerin ise en erken sipariş tarihinde ve teslim tarihinde bağlayacağına dikkat edin. Sipariş tarihi sütununu veya Başlangıç tarihini Zamanlama Ayrıntıları Hızlı Kutusundan doğrulayın.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]