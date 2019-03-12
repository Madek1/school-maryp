<template>
  <div id="article-content">
    <p v-if="text1[articleId - 1]" class="first-paragraph">{{ text1[articleId - 1] }}</p>
    <p v-if="text2[articleId - 1]" class="second-paragraph">{{ text2[articleId - 1] }}</p>
    <p v-if="text3[articleId - 1]" class="third-paragraph">{{ text3[articleId - 1] }}</p>
    <p v-if="text4[articleId - 1]" class="fourth-paragraph">{{ text4[articleId - 1] }}</p>
    <p v-if="text5[articleId - 1]" class="fifth-paragraph">{{ text5[articleId - 1] }}</p>
  </div>
</template>

<script>
export default {
  name: "ArticleContent",
  data() {
    return {
      text1: [
        `Już wstążkę pawilonu wiatr zaledwie muśnie,\n
        Cichymi gra piersiami rozjaśniona woda;\n
        Jak marząca o szczęściu narzeczona młoda\n
        Zbudzi się, aby westchnąć, i wnet znowu uśnie.`,
        `Bywają straszne noce: wiatr deszczem tnie chłodnym,\n
        Mgieł opona strzępami po morzu się ściele....\n
        W takie noce złym duchom i upiorom wodnym\n
        Jest czas harców bezecnych i wielkie wesele.\n`,
        `Chodź do mnie, pielgrzymie stęskniony,\n
        Na moje błękitne przezrocze:\n
        Dam tobie majestat korony,\n
        Wieńcami cię pereł otoczę...\n`,
        `Nad modrą toń wykwitły, trysnęły kaskadą,\n
        Na roztrzęsionych piórach niosą morza piany,\n
        Lecą w słońce, jak obłok złotem malowany,\n
        I wiankiem się róż białych na powietrzu kładą.\n`,
        `O ciche, ciche morze! Gdyby w twe odmęty można\n
        paść i znicestwieć w twoich wód ogromie…\n
        Nie chciałbym istnieć więcej, nawet nieświadomie,\n
        gdy przejdę przeznaczeniem szlak życia wytknięty.\n`,
        `Pamiętasz? Było kiedyś morze\n
        szkliste w falistych linii łukach,\n
        morze, którego cieni można\n
        w obrazach szklanych dni poszukać...\n`,
        `Cisza płonie w przestworzu,\n
        Morze coraz ciemniejsze,\n
        Gwiazdki, nawet najmniejsze,\n
        Odbijają się w morzu\n`,
        `Morze aż śmiesznie piękne, nieprawdopodobne,\n
        Zupełnie nieprawdziwe, wprost niedopuszczalne:\n
        Tak ciemnofijołkowe szalonym szczęściem triumfalne.\n`,
        `O morze! sine morze! kto nad cię piękniejszy?\n
        Z wszystkich Stwórcy objawień, kto większy od ciebie?\n
        Nic twych wdzięków nie zgasi, wielkości nie zmniejszy,\n
        Piękneś w obliczu ziemi, i piękne przy niebie,\n
        I wielkie i ogromne, jakby Bóg cię stworzył,\n
        Aby wieczność wysławił, ludzi upokorzył.\n`
      ],
      text2: [
        `Żagle, na kształt chorągwi gdy wojnę skończono,\n
        Drzemią na masztach nagich; okręt lekkim ruchem\n
        Kołysa się, jak gdyby przykuty łańcuchem;\n
        Majtek wytchnął, podróżne rozśmiało się grono.`,
        `Wśród powodzi fal groźnych,toczących się z szumem,\n
        Słychać dzikie wołania, jęki tajemnicze;\n
        Czasem we mgle przelecą jakieś widma tłumem,\n
        Czasami się wychyli upiora oblicze....\n`,
        `Posłuchaj, jak szemrzą głębiny,\n
        Jak pluszcze w kryształach kaskada:\n
        O cudach bajecznej krainy\n
        Bezduszny tam głaz opowiada.\n`,
        `Giną, gasną, uchodzą w tęczę jakąś bladą…\n
        Wtem ciśnie zdechłą rybę pachoł wpółpijany.\n
        A wnet ostrzem przecina błękitny krzyk szklany\n
        I na żertwę spadają zwichrzoną gromadą.\n`,
        `Poznanie krew zamienia w proch, piołun i męty,\n
        truciznę w każdym duszy zaszczepia atomie,\n
        nieprzyjaciel straszliwy, pełznący kryjomie,\n
        nigdy niewyczerpany i zawsze zawzięty.\n`,
        `Morze czasami wzbierające\n
        roznosem huku na poszumach,\n
        szelestem w dali zamykanym\n
        na stoodległych górskich szumach.\n`,
        `Ośmielone milczeniem,\n
        Rozpalone tą ciszą,\n
        Drżą leciutko i wiszą\n
        Ponad wody złocieniem.\n`,
        `Wobec tego już wszystko chyba stać się może,\n
        Zwłaszcza, że brak tu ludzi, by nie dali wiary:\n
        Fale wyciągną ręce i zaczną w ferworze\n
        Klaskać... Już idzie z lutnią ślepy Homer stary.\n`,
        `Czy słońce się przegląda w twej zielonej fali,\n
        I, topiąc swe promienie w przezroczyste głębie,\n
        Stem barw ciebie ubiera, płomieniem zapali,\n
        Lub maluje, jak opal, jak szyje gołębie,\n
        Czy noc czarna zapadnie, Menes wejdzie blady,\n
        I strugą światła srebrną wysypie swe ślady –\n`
      ],
      text3: [
        ` O morze! pośród twoich wesołych żyjątek\n
        Jest polip, co śpi na dnie, gdy się niebo chmurzy\n
        A na ciszę długimi wywija ramiony.`,
        `Od jednego wód krańca aż po drugi kraniec,\n
        Zanim blady świt hasło do powrotu poda,\n
        Cała siła piekielna w zamęcie się nurza :\n`,
        `A jeśli, natchnieniem owiany,\n
        Zapragniesz ulecieć na smugi,\n
        Rozpięte wśród niebios namiotu,\n`,
        `O serce, między niebem a ziemią zaklęte!\n
        Serce, rozjęciem skrzydeł na zorzach aż święte,\n
        Anielskie wzloty twoje w jutrzenkach się ważą…\n`,
        `Tam, w tych przepaściach wodnych przepaść jak żwir z brzegu,\n
        nic nie czuć, nic nie pragnąć, wszystko zrzucić z siebie,\n
        na zawsze się wymazać z dal i dusz szeregu…\n`,
        `Morze płączące świstem deszczu\n
        i perłopiawiem pianorodne,\n
        dalekie, ciche, smutne głębią\n
        jak moje oczy twoich głodne.\n`,
        `Ale tak są malutkie,\n
        Wyglądają tak blado,\n
        Że ze wstydu i smutku\n
        Na dno morza się kładą.\n`,
        null,
        `Ty zawsze wielkie, piękne, ty zawsze cudowne!\n
        Oko ludzkie, co na twych przestrzeniach spoczywa,\n
        Drogie myśli z twych głębin, obrazy czarowne,\n
        Droższe pereł, korali, nurzając, dobywa;\n
        A ucho, twego głosu słuchając zdumiałe,\n
        Zda się słyszy, jak w niebie nucą Bożą chwałę.\n`
      ],
      text4: [
        ` Co śpi wpośród złych losów i namiętnej burzy;\n
        O myśli! w twojej głębi jest hydra pamiątek,\n
        A gdy serce spokojne, zatapia w nim szpony.\n`,
        `Rośnie, huczy, szaleje sądnego dnia taniec,\n
        Aż w Niebo ryk uderza, aż pali się woda !\n
        Sama śmierć im przygrywa, przyśpiewuje burza....\n`,
        `Ja szlak ci uwiję różany,\n
        Dam tobie swe wichry za sługi\n
        I skrzydła tęczowe do lotu!\n`,
        `Lecz niech los-pachoł ciśnie wpółzgniłą zanętę,\n
        Wnet ty, o najsrebrzystsze, ty, o wniebowzięte\n,
        Z krzykiem żądzy nań spadasz i zwierzęcą twarzą.\n`,
        `Tam – nic nie chcę… Na wieki niechaj mię pogrzebie\n
        jakiś odmęt, niech zginę tak i znicestwieję,\n
        jak nicestwieją w życiu wiary i nadzieje…\n`,
        `Morze przebite nocą w gwiazdy\n
        powraca czasem cicho, jaśnie,\n
        morze potęgi i miłości,\n
        które w twych oczach cicho gaśnie.\n`,
        null,
        null,
        `Ciche, tyś wielkie, straszne w swoim majestacie,\n
        W lazurem, zielonością wyszywanej szacie,\n
        Zburzone, ty falami bijąc brzeg zszarpany,\n
        Rycząc, z wnętrzności białe wyrzucając piany,\n
        Trwogą napełniasz serce, dusze niepokojem,\n
        Jakbyś ziemię pochłonąć chciało w łonie swojem.\n`
      ],
      text5: [
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        `Morze! czemuż ten, co cię pokochał namiętnie,\n
        Jak pierwszą miłość w duszy, pamięć twoją chowa,\n
        I wspomina o tobie z uniesieniem, smętnie?\n
        We snach ku twoim brzegom zwraca mu się głowa\n
        I serce na szmer fali podnosi się twojej,\n
        A w oczach wciąż twa wielkość i piękność mu stoi?\n`]
    };
  },
  props: {
    articleId: Number(String)
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
#article-content {
  white-space: pre-wrap;
  width: 500px;
  margin: 0 auto;

  p{
    margin: 40px 0;
    text-align: left;

    &::first-letter {
      font-size: 32px;
      margin-left: 30px;
    }
  }
}
</style>
