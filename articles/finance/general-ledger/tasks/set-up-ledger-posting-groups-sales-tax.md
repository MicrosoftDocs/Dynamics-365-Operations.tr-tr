---
title: Satış vergisi için Genel muhasebe deftere nakil grupları ayarlayın
description: Satış vergisi hesaplanır ve Genel muhasebe deftere nakil gruplarında belirtilen ana hesaplara nakledilir.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1860f338faf357ecb8faa04cc687a6ec08cdc6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222275"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Satış vergisi için Genel muhasebe deftere nakil grupları ayarlayın

[!include [banner](../../includes/banner.md)]

Satış vergisi hesaplanır ve Genel muhasebe deftere nakil gruplarında belirtilen ana hesaplara nakledilir. Genel muhasebe deftere nakil grupları, her bir satış vergisi koduna eklenir. Her satış vergisi kodu için ayrı ayrı genel muhasebe deftere nakil grupları ayarlayabilir, bir genel muhasebe deftere nakil grubunu tüm satış vergisi kodları için kullanabilir veya satış vergisi kodlarına birden fazla genel muhasebe deftere nakil grubu atayabilirsiniz. Bu kayıtta DEMF demo şirketi kullanılmaktadır. 

1. **Gezinti bölmesi > Modüller > Vergi > Kurulum > Satış vergisi > Genel muhasebe deftere nakil grupları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Genel muhasebe deftere nakil grubu** alanına bir değer girin.
4. **Tanım** alanına bir değer girin.
5. **Satış vergisi borcu** alanında, vergi dairesine borç yazılacak giden satış vergileri için ana hesabı seçin. Vergiye tabi mal ve hizmetler satıyorsanız, satış vergileri, vergi makamı adına tahsil edilir.  
6. **Satış vergisi alacağı** alanında, vergi dairesinden alınacak gelen vergiler için ana hesabı seçin. Vergiye tabi mal ve hizmetler satın alıyorsanız, vergileri, vergi makamı adına satıcılar tahsil eder. **Genel muhasebe parametreleri** sayfasında Satış vergisi vergilendirme kurallarını uygula seçeneği belirtildiyse bu alan kullanılmaz. Bunun yerine, satıcılara ödenen satış vergileri, satın almada kullanılan hesaba borç kaydedilir.   
7. **Kullanım vergisi gideri** alanında, AB ters gider GST/HST'sinin bir parçası olarak satıcıların vergi dairesinden talep etmediği veya vergi dairesine bildirmediği, vergiden düşülebilir Kullanım vergileri için ana hesabı seçin. Harekette kullanılan **Satış vergisi grubunda** **Satış vergisi kodu** için **Kullanım vergisi** seçeneğinin belirtilmelidir. **Genel muhasebe parametreleri** sayfasında **Satış vergisi vergilendirme kurallarını uygula** seçeneği belirtildiyse bu alan kullanılamaz.   
8. **Kullanım vergisi borcu** alanında, vergi dairelerine borç yazılacak giden Kullanım vergilerini nakletmek için ana hesabı seçin. **Kullanım vergisini** nakletmek için, **Satış vergisi grubunda** **Satış vergisi kodu** için **Kullanım vergisi** seçeneğini belirtilmelidir. **Genel muhasebe parametrelerinde** **Satış vergisi vergilendirme kurallarını uygula** seçeneği belirtilirse, mahsubun hareket gider hesabına nakledilmesi gerekir.   
9. **Kapatma hesabı** alanında, **Kullanım vergisi borcu** ve **Satış vergisi alacağı** alanlarında belirtilen genel muhasebe hesaplarının net bakiyesinin nakledileceği ana hesabı seçin. Satış verigileri kapatılınca ve deftere naklet işi çalıştırılınca bakiye oluşturulur.  Kapatma döneminin vergi dairesi bir satıcı hesabıyla ilişkilendirilmişse, bakiye, satıcı hesabına nakledilecektir.
10. **Satıcı nakit iskontosu** alanında, bu Genel muhasebe deftere nakil grubuyla ilişkili Satış vergisi kodları için nakit iskontosunun nakledileceği ana hesabı seçin. Bu, isteğe bağlıdır ve hiç hesap girilmezse, **Nakit iskontosu kodlarındaki** ana hesap kullanılır. Satış vergisi gruplarında Nakit iskontosundaki ters satış vergisi seçeneği kullanılıyorsa, **Genel muhasebe deftere nakil grubu** başına farklı hesaplar kullanırken yararlı olabilir.  
11. **Müşteri servis talebi iskontosu** alanında, bu **Genel muhasebe deftere nakil grubuyla** ilişkili **Satış vergisi kodları** için nakit iskontosunun nakledileceği ana hesabı seçin. Bu, isteğe bağlıdır ve hiç hesap girilmezse, **Nakit iskontosu kodlarındaki** ana hesap kullanılır. **Satış vergisi gruplarında** Nakit iskontosundaki ters satış vergisi seçeneği kullanılıyorsa, **Genel muhasebe deftere nakil grubu** başına farklı hesaplar kullanırken yararlı olabilir.  
12. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]