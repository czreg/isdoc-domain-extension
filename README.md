ISDOC extenze pro zpracování informací o doménách
=================================================

Faktury na registrace a prodloužení doménových jmen a souvisejících služeb obsahují
většinou i informace o jménu domény a o dni začátku a konce poskytnutí služby. Tyto
informace nelze vložit do standarního ISDOC, který ale umožňuje rozšíření jeho definice.

Sdružení registrátorů CZ.REG z.s.p.o. připravilo ISDOC extenzi pro standardizovaný
zápis jména domény a data začátku a konce poskytování služby ke každému řádku faktury.
Extenzi lze u každého řádku použít vícenásobně, jedním řádkem tak lze vyúčtovat jednu
nebo více domén.

Použití extenze je u každého řádku faktury volitelné. Pokud je extenze použita je 
povinné uvedení jména domény, zatímco data jsou volitelná.

Schema je v souboru _schema/czreg-domain-1.0.xsd_

Extenze musím mít nastavený jmenný prostor na _http://czreg.cz/isdoc/namespace/domain-1.0_.

Příklad řádku faktury s extenzí pro domény s uvedením dvou domén na jednom řádku:

        <InvoiceLine>
            <ID>1</ID>
            <LineExtensionAmount>14.5</LineExtensionAmount>
            <LineExtensionAmountTaxInclusive>17.4</LineExtensionAmountTaxInclusive>
            <LineExtensionTaxAmount>2.9</LineExtensionTaxAmount>
            <UnitPrice>14.5</UnitPrice>
            <UnitPriceTaxInclusive>17.4</UnitPriceTaxInclusive>
            <ClassifiedTaxCategory>
                <Percent>20.0</Percent>
                <VATCalculationMethod>0</VATCalculationMethod>
            </ClassifiedTaxCategory>
            <Item>
                <Description>register</Description>
            </Item>
            <Extensions>
              <Domains xmlns="http://czreg.cz/isdoc/namespace/domain-1.0">
                <Domain>
                    <Name>first.cz</Name>
                    <Since>2011-08-22</Since>
                    <Till>2012-08-21</Till>
                </Domain>
                <Domain>
                    <Name>second.cz</Name>
                    <Since>2011-08-22</Since>
                    <Till>2012-08-21</Till>
                </Domain>
              </Domains>
            </Extensions>
        </InvoiceLine>

Autoři
------
* Jiří Kubíček <jiri.kubicek@kraxnet.cz>
* Josef Pospíšil <josef.pospisil@laststar.eu>
