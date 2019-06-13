<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="payinvoice.md" target-language="tr-TR">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>payinvoice.758282.b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\payinvoice.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up pay invoice scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fatura ödeme senaryolarını ayarlama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to configure Dynamics 365 for Retail to support various scenarios relating to invoice payments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu konuda, Dynamics 365 for Retail'ın nasıl fatura ödemeleriyle ilgili çeşitli senaryoları destekleyecek şekilde yapılandırılacağı açıklanmaktadır.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up pay invoice scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fatura ödeme senaryolarını ayarlama</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail'daki Fatura öde işlevi aşağıdakileri destekleyecek şekilde genişletilmiştir:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Payoff of multiple sales order invoices in a single POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tek bir POS hareketinde birden fazla satış siparişi faturasının ödenmesi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Serbest metin faturaları, proje tabanlı faturalar ve alacak dekontları gibi çeşitli müşteri faturası türlerinin ödenmesi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bu senaryoları etkinleştirmek üzere, mağazalar için işlev profilinin aşağıda belirtildiği gibi yapılandırılması gerekir.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Channel setup <ph id="ph2">\&gt;</ph> POS setup <ph id="ph3">\&gt;</ph> POS profiles <ph id="ph4">\&gt;</ph> Functionality profiles<ept id="p1">**</ept> and select a profile that's linked to the stores that you want to make the changes for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Perakende <ph id="ph1">\&gt;</ph> Kanal ayarı <ph id="ph2">\&gt;</ph> POS ayarı <ph id="ph3">\&gt;</ph> POS profilleri <ph id="ph4">\&gt;</ph> İşlev profilleri<ept id="p1">**</ept>'ne gidin ve değişiklikleri yapmak istediğiniz mağazalarla ilişkili bir profil seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>On the <bpt id="p1">**</bpt>Functions<ept id="p1">**</ept> tab, configure the following parameters as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>İşlevler<ept id="p1">**</ept> sekmesinde, aşağıdaki parametreleri gerektiği gibi yapılandırın.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Sales order invoice<ept id="p1">**</ept> – Select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to allow users to pay one or more sales order-based invoices in a single POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Satış siparişi faturası<ept id="p1">**</ept>: Kullanıcıların tek bir POS hareketinde bir veya daha fazla satış siparişi tabanlı faturayı ödemesine izin vermek için <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept>'i seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Free text invoice<ept id="p1">**</ept> – Select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to allow users to pay one or more free text-based invoices in a single POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Serbest metin faturası<ept id="p1">**</ept>: Kullanıcıların tek bir POS hareketinde bir veya daha fazla serbest metin tabanlı faturayı ödemesine izin vermek için <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept>'i seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Project invoice<ept id="p1">**</ept> – Select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to allow users to pay one or more project-based invoices in a single POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Proje faturası<ept id="p1">**</ept>: Kullanıcıların tek bir POS hareketinde bir veya daha fazla proje tabanlı faturayı ödemesine izin vermek için <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept>'i seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Sales order credit note<ept id="p1">**</ept> – Select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Satış siparişi alacak dekontu<ept id="p1">**</ept>: Kullanıcıların birden fazla satış siparişi tabanlı alacak dekontunu açık faturalara göre kapatmasına veya açık bir alacak dekontu için bir geri ödeme işlemi yapmasına izin vermek için <bpt id="p2">**</bpt>Evet<ept id="p2">**</ept>'i seçin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Payment or settlement of partial amounts is not yet supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kısmi tutarları ödeme veya kapatma henüz desteklenmemektedir.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>