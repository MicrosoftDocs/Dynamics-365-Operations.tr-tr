---
title: "Mali takvimler, mali yıllar ve dönemler"
description: "Bu makalede, mali takvimler, mali yıllar, mali dönemler ve bunların tüzel kişilikler, sabit kıymetler ve bütçeleme için nasıl kullanıldığı ele alınmaktadır."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: aafb0d0c7d262311714ff81765e10337c5a0d78a
ms.lasthandoff: 03/31/2017


---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Mali takvimler, mali yıllar ve dönemler

Bu makalede, mali takvimler, mali yıllar, mali dönemler ve bunların tüzel kişilikler, sabit kıymetler ve bütçeleme için nasıl kullanıldığı ele alınmaktadır.

Mali takvimler bir kuruluşun finansal faaliyeti için bir çerçeve sağlar. Her mali yıl takvimi bir veya birden çok mali yıl içerir ve her bir mali yıl, birden fazla dönem içerir. Mali takvimler 1 Ocak ile 31 Aralık takvim yılına veya seçtiğiniz herhangi bir tarih aralığına dayalı olabilir. Örneğin, bazı kuruluşlar bir yılın 1 Temmuz'unda başlayan ve sonraki yılın 30 Haziran'ına kadar süren bir mali takvimi seçerler. 

Oluşturabileceğiniz mali takvimlerin sayısı için bir sınır yoktur ve bir mali takvim için oluşturulan mali yıl sayısı için de sınır yoktur. Her mali takvim kuruluşunuzdan bağımsızdır ve kuruluş içindeki birden çok tüzel kişilikler tarafından kullanılabilir. Örneğin, bir kuruluşun sekiz departmanı vardır ve her departman ayrı bir tüzel kişiliktir. Bunların beşi aynı mali takvimi paylaşır ve üçü farklı mali takvimleri kullanır. Aynı mali takvimi paylaşan beş tüzel kişilik için bir mali takvim ve sonra diğer tüzel kişilikler için ayrı bir mali takvim oluşturabilirsiniz.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Mali takvimler, mali yıllar ve dönemler oluşturmak
Mali takvimler, mali yıllar ve dönemleri Mali takvimler sayfasında oluşturabilirsiniz. Ayrıca mevcut dönemleri bölmek ve bir mali yılı sonlandırmak için kapanış dönemleri oluşturabilirsiniz. 

Kapanış dönemi, mali yıl kapatılırken oluşturulan genel muhasebe hareketlerini ayırmak için kullanılır. Kapanış hareketlerinin bir mali dönem içinde olduğunda, farklı türde kapatma girişlerini dahil edilecek veya dışarıda bırakılacak mali tabloları oluşturmak çok kolaydır. Eğer bir mali yıl 12 mali döneme ayrılmışsa, kapanış dönemi genellikle 13th dönemdir. Ancak, bir kapanış dönemi, durumu açık olan herhangi bir dönemden oluşturulabilir. 

Kapanış dönemi oluşturduğunuzda, durumu Açık olan bir dönem seçin ve kullanmak istediğiniz tarihleri olan. Yeni bir kapanış dönemi mevcut dönemin başlangıç ve bitiş tarihlerini kopyalar. Asıl dönem var olmaya devam eder. Örneğin, mali yılın son döneminden olduğu ve 1 Ağustos-31 Ağustos tarihleri olan 12 dönem, seçin. Size yakın gibi bir kapanış dönemi için bir ad girin. Yeni kapatma periyodunu oluşturduktan sonra artık özgün döneme ve kapanış dönemine sahipsiniz. Her ikisinin de 1 Ağustos tarihinde başlayıp ve 31 Ağustos'ta biten tarihleri vardır.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Genel muhasebeler, sabit kıymetler ve bütçe döngüleri için mali takvim seçin
Mali takvimler sabit kıymet amortismanı, mali hareketler ve bütçe döngüleri ile kullanılır. Mali takvim oluşturduğunuzda, birden çok amaç için kullanabilirsiniz. Sabit kıymet takvimi yapmak için, bir değer modeli veya amortisman defteri için mali takvim seçebilirsiniz. Genel muhasebe defter takvimi yapmak için bir mali takvim seçebilirsiniz. Bütçe takvimi yapmak için bir bütçe döngüsüne mali takvim seçebilirsiniz. Bunların tümü için aynı mali takvimi kullanabilirsiniz.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Tüzel kişiliğiniz için bir mali takvim seçin

Genel muhasebe defter formunda, bir tüzel kişiliğinizin genel muhasebe defterinde kullanmak istediğiniz mali takvimi seçin. Her bir tüzel kişilik için bir mali takvim, Genel muhasebe defteri sayfası üzerinden seçilmelidir. Bit mali takvimi seçtikten sonra, mali yılın parçası olan tüm dönemler için dönem durumları ve izinleri Genel muhasebe defter takvimi sayfasından ayarlayabilirsiniz.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Sabit kıymetler için bir mali takvim seçin

Bir değer modeli veya amortisman defteri için bir mali takvim seçebilirsiniz. Bu mali takvim daha sonra seçili değer modelini veya amortisman defterini kullanan sabit kıymetler tarafından kullanılacaktır. Mali takvimler sayfasında tanımlanan herhangi bir mali takvim arasından seçim yapabilirsiniz.

### <a name="define-budget-cycle-time-spans"></a>Bütçe döngüsü zaman aralıklarını tanımlayın

Bütçe döngüleri, bütçenin kullanıldığı zaman uzunluklarıdır. Bütçe döngüleri bir veya birden fazla mali yılın bir parçasını içerebilir, örneğin iki yıllık için biennial bütçe döngüsü veya üç yıllık için triennial bütçe döngüsü gibi. Bütçe döngüsü zaman süreci, bütçe döngüsüne dahil edilen dönemlerin sayısını tanımlar. Bütçe döngüsü zaman sürecini belirlemek için, Bütçe döngüsü zaman süreçleri sayfasını kullanın.

## <a name="maintain-periods-for-your-organization"></a> Kuruluşunuz için dönemlerini korumak
Genel muhasebe defteri takvimi sayfasını, kuruluşunuz tarafından kullanılan mali takvimin, mali yılların ve dönemlerin ayrıntılarını görüntülemek için kullanabilirsiniz. Dönemlerin durumu değiştirmek ve hangi kullanıcıların hesap dönemlerine hareketleri deftere nakledebilmeniz için seçin. Örneğin, yeni bir dönemin başlangıcında, diğer gruplar yalnızca yeni dönemde çalışırken önceki dönemde, mali hareketleri deftere nakil bitirmek için bir kullanıcı grubu isteyebilirsiniz.




