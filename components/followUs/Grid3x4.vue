<template>
  <div
    class="grid grid-cols-3 gap-3 overflow-hidden w-full relative left-[3.75rem]"
  >
    <!-- relative -top-[48px] -->
    <div class="grid gap-3 *:rounded-xl *:overflow-hidden relative top-[-35px]">
      <div v-for="(img, index) in imgList1" :key="index">
        <img class="h-[238px] w-[238px]" :src="img" alt="" />
      </div>
    </div>
    <!-- relative -top-[100px] -->
    <div class="grid gap-3 *:rounded-xl *:overflow-hidden">
      <div v-for="(img, index) in imgList2" :key="index">
        <img class="h-[238px] w-[238px]" :src="img" alt="" />
      </div>
    </div>
    <!-- relative -top-[34px] -->
    <div class="grid gap-3 *:rounded-xl *:overflow-hidden relative -top-[34px]">
      <div v-for="(img, index) in imgList2" :key="index">
        <img class="h-[238px] w-[238px]" :src="img" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup>
const imgList1 = [
  "https://s3-alpha-sig.figma.com/img/7f4b/5a65/f55914a7114487c93d67eda7d5837992?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=A5ODj~yFNTDWLXsT33Z6DY37BM3W8AxpKgAkX-LOBwUCNURRfIU5xNHZSE3souhJSWz3xerNeeuZ3nBa1f6k0GLqV~Kd57lUgSSc73cGeEofgBh0DA9aVFuOWATOyukw564pid-FQdbXIChCgCsgyzzs5YoYBYGPkkfiCO9KObhYtEZ6Qq2g4QO4-SfuLHowKM53qNBHGjfnjiSi53t-Rvm9yv5iE3-A6vT2jqvbhovrwnjM4PPvnOD6~2-8KtxmYpzi5B-VMHD2xv7Z76Xurmpd0q~S13zgXUXDSgc9p4CazjC3TdKo1hB9F6TjMvqS0TgwJExilQ62mnQoYl-0ww__",

  "https://s3-alpha-sig.figma.com/img/c188/b404/98eed20749723698bb71095b6956fc21?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=BV9x7-S4EC6XltLZqF0KvOmWDpIX~xW-CLO5JeuOJp50CNtLGVkTJA8HRYg9N0QzMPS8aSUAkbw36aXswV69IayhDU-XJlEVEOBuNXrk83f~~PfO1KtExsUjRdba34Hf999m3tcG-eq~QqA9tHcWwXqPFD6fvls0SnjbdvsnZ7XH1WnEQ-EsMVDlrXDdquVIDwmq31USvet3d~OVJNKWs5TfOVvxobwDLMaGxGQXS8bsakaPOQUOMGhawl~CY-e7A96jX951GYTMwnHsqH97DfTCzyM6ju8arI2Xmo7d8~2PcqHMyX2QCPeqn5Rp5XjyGvfwKLeN2n67IMhZjkkdrw__",

  "https://s3-alpha-sig.figma.com/img/bae7/70c7/9e15cd08ca975d9433cf8e93651af5d3?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=c2PyNrJCDqzEYBVvZvQ0mSfJWDbRV8MpPFPF0QI2vhvN6LK9ZQOq~VpGheV1cZDoSnVk978xsxXBKK4Do3YBUr9zobDh5umiEK~YLZMrOW~iputE5pKxl-WVx2AKSrQ-2bTlQq63ijgj7QwPkf00GFLmzQNX~3J0yuzoTg3oXhRRsj7HFqEs334ACymfup7pFPjVBGxuv7uDKs4MXje69rBYLPD6wN2ejuiOf5gPfGP5VJS0c6MiUuz6SpTY3dkpxZ45wZPT2eR3Mu4xUYmT3h73B8NUG7Fdtxja8ErKFRs2VuksmV50zvIt0Vq0K8Fp~VtSe743--Pi4eZGLMkfkw__",

  "https://s3-alpha-sig.figma.com/img/8ad1/ecb1/74528ca2cfdb5f0e93b6cfe114dfb0a0?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=C1KxNyOEIili-IhRCTiVumgEYVUxzp-wdUfWb3N7WbGut2i8JtjYuX-foDPv3emcEmmYQi0LDWbMFEb6DeVN~QKsINRZp01w1Q-wq6zPRDpmFExkmWwvsdjcT7xBVPrYMiydTdvc70LltS6ZmCktZb5OPJSdjhj3OCasp-6jY5LViYFHlnfr50hV6tTnIGhnVMajpUjTBdRIdCQUZU98dkU7p6XaHQumJsoliTVumQGVUSFgN756aJccwNqn~CsVjpNWLa0XYJqrIIrezcG7raP0hsj17u0kGrWGQP1jeruiAviaKABHltOqNjmXvYEfPzgrYxH~9xKwxPKETYwRbQ__",
];
const imgList2 = [
  "https://s3-alpha-sig.figma.com/img/c6dd/fac9/85064819d738a80aba911737fdca1810?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=YO7s7u-AZJMkmffw0mgnxI9lXJfqQ~-Ccol42NtoTUQQQeOUNXmFN8kewxlj4ZYviDAQQru0IpHEfcFc4PUy2FwI6ueDCZs9U~v2XlZ3KA-Re~UkSaPjgKfprzE0OXcuixwrStA2s3ne-gvP~~cXbgbzqruGQo~o72tWv~u3Bcip3Em0jD-9zy-OdoWDWz-96Dd5eGnaK1zlfo9~AEKVB2uUU4SwtjJ5EhfFujiuMI4Z6uZ-0Ib1c4Kpv6O-uP~6WlraWpKWt~ts8F-2qvkPd-URxp28h21uVNrwuObvIgkVGjHW~t0L8ryZq83RDxwpjBstjg5H6qf~fAaxFDxEwQ__",

  "https://s3-alpha-sig.figma.com/img/483f/3d72/1b90325b6a0317617c5b3d5f8ccaf6be?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=WohUe19yo~KUcCdgFQRU7MR6hpLp21e~C309pKijpP5Ul0S4fyJMe6tUm74sbqt~dEVd1JHxeMTCZiKZD9BSQrdTCHFgnxZx6IViUXywcXzsn95WFgxiijD2fDVrVcNcTOikGFEvk76w9cbBBspgfXt0BZ8bBf1258w2bOgsgzU~NaUipzAe74Ncon~nxkUT6Pwrb4AtXaAjbF6kxCJY4SUpDy~gYAvXRZTLo0MQcFzn637VRRnh-kmF-U9ZzMB8ImrbA0yX30gTtgBbJXlrMBk6IRE~g0OuoBexJ5C-fLPBjqZneV0XzIJMOIIZbzjXmV6XkvJS1u1ylUko5RFfzw__",

  "https://s3-alpha-sig.figma.com/img/1751/3529/cee984044d14150af7bc2aeaecf7f723?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=B032PmgQZreZJfHqMfA-3BEY5i95uBDdGodOpK8Ln0aCesGdCzTwE02QIpVe2fa9No7pVsmrCQ267qGTRMZntR3~ideZzm8EEy6~k~aVW08GldOTav39~6sqdm8Q9DNiYb1Z~zvhZBMwjcjyr-ACg7dQ4FhZ3JE1UgNYWT6jdwPJOJ6-hNoBjeAh8UWcBAhPJCrGfRVcaMLx4lhF9m9ObxQ5yB0szViyMIgpgdqwWXnn~rtLxEIBz8KK7OrVIgJXrBW8A1f7sL4VxDkDu9Q8qHaHtFTSGnEqnrasmos41HL3EngPAWc-~FtrxjuFP-IVVOn4~kQxkm5-b8Jma3Yd1g__",

  "https://s3-alpha-sig.figma.com/img/6141/0f28/073ffa6f3ec5f84a4d222ffb1c315da1?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=NoBZcNQXlSlDpwrmq0gWBfmfouI8qbx46xDgt~pe4siyC7tTxANX01r~KoOzriKpEu3iCNgMHdlOKNLPLJ2W3iftkNx-lrM44vETe9x8gLBXMdgrML~Tj4KnQq1DvG8n-BiwPRLSDvzcVOQi5FIIxTjS6GqP4rqdllWs1tkXgfMAefa7sK~pYwWpjwAaCwC~nVC~vcjdz36SHQw4muUD5roHXmqd2HwRXPD~-ZW3G4ZRZ8H8JQ0q~uxkaaxk474N5MNKbjV6qjZH~5TrrEw0VB9LOxI9qwSZcP-tyjkCwpEVQsc2Scfl80M-krVNr7LoUZcaD6DtqeBeYtlJsE7kow__",
];
const imgList3 = [
  "https://s3-alpha-sig.figma.com/img/640f/fc0b/7e46c5838971f2e4d23a947c665b6507?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=a49QND9xEiYxNV9FoWL-2~~orYEw715uIwAjYeoZKMZfQeFKDtAO9bwO9wJZG5mWxbOnKFW7WVu57uqyMEi2dqujiIcqSV5JoN0oNa5gWl4tDwt31O3NQQYU~iY67qaI3xauaZCgclPW~P5-8jFcp8Jloa6tmOLQYdb0GVdevg2HT~9AAPdq~tVWSnpwUiMSIIAwI39LzfMnjRrQ2zlA8H-DSfSgLZxz93bto9PEd71qt-4MGlb5-0Zl~4ZWz1YuxAEuyHwAaDJUP1vtIE6dJBYw~8Bd603cTprmU6hRU29j1-HUgcgVBjpL2RaGcXuIyAH2vuI1NonEIpIrweO3xA__",
  "https://s3-alpha-sig.figma.com/img/c188/b404/98eed20749723698bb71095b6956fc21?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=BV9x7-S4EC6XltLZqF0KvOmWDpIX~xW-CLO5JeuOJp50CNtLGVkTJA8HRYg9N0QzMPS8aSUAkbw36aXswV69IayhDU-XJlEVEOBuNXrk83f~~PfO1KtExsUjRdba34Hf999m3tcG-eq~QqA9tHcWwXqPFD6fvls0SnjbdvsnZ7XH1WnEQ-EsMVDlrXDdquVIDwmq31USvet3d~OVJNKWs5TfOVvxobwDLMaGxGQXS8bsakaPOQUOMGhawl~CY-e7A96jX951GYTMwnHsqH97DfTCzyM6ju8arI2Xmo7d8~2PcqHMyX2QCPeqn5Rp5XjyGvfwKLeN2n67IMhZjkkdrw__",
  "https://s3-alpha-sig.figma.com/img/1751/3529/cee984044d14150af7bc2aeaecf7f723?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=B032PmgQZreZJfHqMfA-3BEY5i95uBDdGodOpK8Ln0aCesGdCzTwE02QIpVe2fa9No7pVsmrCQ267qGTRMZntR3~ideZzm8EEy6~k~aVW08GldOTav39~6sqdm8Q9DNiYb1Z~zvhZBMwjcjyr-ACg7dQ4FhZ3JE1UgNYWT6jdwPJOJ6-hNoBjeAh8UWcBAhPJCrGfRVcaMLx4lhF9m9ObxQ5yB0szViyMIgpgdqwWXnn~rtLxEIBz8KK7OrVIgJXrBW8A1f7sL4VxDkDu9Q8qHaHtFTSGnEqnrasmos41HL3EngPAWc-~FtrxjuFP-IVVOn4~kQxkm5-b8Jma3Yd1g__",
  "https://s3-alpha-sig.figma.com/img/8ad1/ecb1/74528ca2cfdb5f0e93b6cfe114dfb0a0?Expires=1725840000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=C1KxNyOEIili-IhRCTiVumgEYVUxzp-wdUfWb3N7WbGut2i8JtjYuX-foDPv3emcEmmYQi0LDWbMFEb6DeVN~QKsINRZp01w1Q-wq6zPRDpmFExkmWwvsdjcT7xBVPrYMiydTdvc70LltS6ZmCktZb5OPJSdjhj3OCasp-6jY5LViYFHlnfr50hV6tTnIGhnVMajpUjTBdRIdCQUZU98dkU7p6XaHQumJsoliTVumQGVUSFgN756aJccwNqn~CsVjpNWLa0XYJqrIIrezcG7raP0hsj17u0kGrWGQP1jeruiAviaKABHltOqNjmXvYEfPzgrYxH~9xKwxPKETYwRbQ__",
];
</script>
