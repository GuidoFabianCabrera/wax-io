<template>
  <div class="app">
    <HomeSectionHero :data="heroItems" />

    <HomeSectionVideo />

    <HomeSectionBrands :data="brandsItems" />

    <HomeSectionImage :data="nft" />

    <HomeSectionVirl :data="virl" />

    <HomeSectionImage :data="launch" />

    <HomeSectionGames :data="games" />

    <HomeSectionImage :data="build" />

    <HomeSectionPlanet :data="planet" />

    <HomeSectionImage :data="collectos" />

    <HomeSectionCapitalize :data="capitalize" />

    <HomeSectionRoadmap :data="roadmap" />

    <HomeSectionAbout :data="about" />

    <HomeSectionCommunity :data="community" />

    <HomeSectionEducational :data="educational" />

    <HomeSectionImage :data="discord" />
  </div>
</template>

<script>
import HomeSectionHero from "@/components/Home/SectionHero";
import HomeSectionVideo from "@/components/Home/SectionVideo";
import HomeSectionBrands from "@/components/Home/SectionBrands";
import HomeSectionImage from "@/components/Home/SectionImage";
import HomeSectionVirl from "@/components/Home/SectionVirl";
import HomeSectionGames from "@/components/Home/SectionGames";
import HomeSectionPlanet from "@/components/Home/SectionPlanet";
import HomeSectionCapitalize from "@/components/Home/SectionCapitalize";
import HomeSectionAbout from "@/components/Home/SectionAbout";
import HomeSectionCommunity from "@/components/Home/SectionCommunity";
import HomeSectionRoadmap from "@/components/Home/SectionRoadmap";
import HomeSectionEducational from "@/components/Home/SectionEducational";

export default {
  components: {
    HomeSectionHero,
    HomeSectionVideo,
    HomeSectionBrands,
    HomeSectionImage,
    HomeSectionVirl,
    HomeSectionGames,
    HomeSectionPlanet,
    HomeSectionCapitalize,
    HomeSectionAbout,
    HomeSectionCommunity,
    HomeSectionRoadmap,
    HomeSectionEducational
  },
  data() {
    return {
      heroItems: [
        {
          title: "<strong>400</strong>K+",
          description: "Daily Unique Visitors",
          image: "images/hero-item-1.png"
        },
        {
          title: "<strong>23</strong>M+",
          description: "Daily Transactions",
          image: "images/hero-item-2.png"
        },
        {
          title: "<strong>12</strong>M+",
          description: "WAX Accounts",
          image: "images/hero-item-3.png"
        },
        {
          title: "<strong>30</strong>K+",
          description: "dApps",
          image: "images/hero-item-4.png"
        }
      ],
      brandsItems: [
        { small: false, image: ["images/saw-logo.png"] },
        { small: true, image: ["images/atari-logo.svg"] },
        { small: false, image: ["images/mattel-logo.png"] },
        { small: false, image: ["images/sf-logo.png"] },
        { small: false, image: ["images/robotech-logo.png"] },
        { small: false, image: ["images/funko-logo.png"] },
        { small: false, image: ["images/bratz-logo.png"] },
        { small: false, image: ["images/daco-logo.png"] },
        { small: false, image: ["images/weezer-logo.png"] },
        { small: true, image: ["images/amc-logo.png"] },
        { small: false, image: ["images/ws-logo.png"] },
        { small: false, image: ["images/hasbro-logo.png"] },
        { small: false, image: ["images/sony-logo.png"] }
      ],
      nft: {
        title: "WAX is a purpose-built NFT blockchain",
        description:
          "WAX provides everything a brand needs to launch a successful NFT collection — from games and dApps to exchanges, digital marketplaces and more.",
        image: "images/nft.png",
        imageMobile: "images/nft-mobile.png",
        background: "white",
        backgroundMobile: "white",
        button: [],
        large: false
      },
      launch: {
        title: "Launch Your NFTs on WAX",
        description:
          "Join the famous brands that have launched successful NFT collections on WAX, including Funko, Topps, Capcom, and more. We’ll guide you through minting and releasing your collection on the WAX blockchain.",
        image: "images/launch.jpg",
        imageMobile: "images/launch-mobile.jpg",
        background: "white",
        backgroundMobile: "",
        button: [{ text: "connect with us", outlined: false }],
        large: true
      },
      virl: {
        title: "vIRL NFTs are the Future of Commerce",
        description:
          "Learn more about how WAX is changing the way people shop, collect, and create value.",
        background: "",
        backgroundMobile: "",
        button: [],
        large: false
      },
      games: {
        title: "Play On WAX",
        description:
          "Picture this: You’ve been playing your favorite battle royale game for a few years, and by this point have a treasure trove of skins and other cosmetics unlocked. Problem is, the game has lost its luster, and now that virtual wardrobe is essentially worthless.",
        background: "",
        backgroundMobile: "",
        button: [{ text: "explore more", outlined: false }],
        large: false,
        items: [
          {
            background: "images/farmers-world-background.jpg",
            logo: "images/farmers-world-logo.png"
          },
          {
            background: "images/farming-tales-background.png",
            logo: "images/farming-tales-logo.png",
            name: "FARMING TALES"
          },
          {
            background: "images/alien-worlds-background.png",
            logo: "images/alien-worlds-logo.png"
          }
        ]
      },
      build: {
        title: "Build on WAX",
        description:
          "Build or upgrade your dApps, games, marketplaces and more on WAX. The WAX Developer Hive offers full documentation, quickstarts, code samples and more. Most importantly, you can be sure you’re building on a secure, eco-friendly blockchain.",
        image: "images/build.png",
        imageMobile: "images/build-mobile.png",
        background: "",
        backgroundMobile: "",
        button: [{ text: "explore more", outlined: false }],
        large: false
      },
      planet: {
        title: "No NFT is more important than the planet.",
        description:
          "WAX is a carbon neutral blockchain that runs on a Proof of Stake system. Meaning, we don’t need supercomputers to wage an energy-sucking battle to complete a single transaction. It’s a lean, green NFT minting machine.",
        background: "white",
        backgroundMobile: "",
        button: [{ text: "learn more", outlined: false }],
        large: false,
        items: [
          {
            title: "Clean & Carbon Free:",
            description: "WAX is certified carbon neutral by ClimateCare",
            image: "images/clean-logo.png"
          },
          {
            title: "More power, less energy:",
            description: "222,000X less than our closest competitor.",
            image: "images/energy-logo.png"
          },
          {
            title: "Shopping not shipping:",
            description: "vIRLs® make CO2 curbing meaningful and fun.",
            image: "images/shopping-logo.png"
          },
          {
            title: "Supports reforestation:",
            description: " Our Carbon offset vIRL® NFTs literally plant trees.",
            image: "images/reforestation-logo.png"
          }
        ]
      },
      collectos: {
        title: "12 Million Collectors and Counting",
        description:
          "<strong>The WAX Cloud Wallet</strong> is your secure gateway to premiere NFT collections, dApps, video games, marketplaces and more. It also makes buying, selling, trading and giving NFTs easier than ever.",
        image: "images/collectors.png",
        imageMobile: "images/collectors-mobile.png",
        background: "white",
        backgroundMobile: "",
        button: [{ text: "create your wallet", outlined: false }],
        large: false
      },
      capitalize: {
        title: "Capitalize on WAX Tokenomics & DeFi",
        description:
          "The WAX tokenomic model marries the explosive growth of NFTs with the superior monetization capabilities of DeFi. Participate and earn rewards in the form of Ethereum Tokens (ETH) and WAXG Governance Tokens.",
        background: "",
        backgroundMobile: "",
        button: [
          { text: "how to participate", outlined: false },
          { text: "github", outlined: true }
        ],
        large: false,
        items: [
          {
            logo: "images/wax-p.png",
            logoMobile: "images/wax-p-mobile.png"
          },
          {
            logo: "images/wax-e.png",
            logoMobile: "images/wax-e-mobile.png"
          },
          {
            logo: "images/wax-g.png",
            logoMobile: "images/wax-g-mobile.png"
          }
        ]
      },
      roadmap: {
        title: "Roadmap",
        description: '<span style="font-size:24px">JUNE 2021</span>',
        background: "",
        backgroundMobile: "",
        button: [],
        large: false,
        items: [
          {
            title: "Development",
            description: "Altcoin Support (ETH Bridge)",
            complete: true
          },
          {
            title: "New Product",
            description: "One stop for WAX NFTs",
            complete: true
          },
          {
            title: "New Product",
            description: "WAX.io revamp",
            complete: true
          },
          {
            title: "Development",
            description: "DeFi Completion",
            complete: false
          },
          {
            title: "WAX Product",
            description: "WAX Cloud Wallet 3.0",
            complete: false
          },
          {
            title: "WAX Product",
            description: "WAX Cloud Wallet Mobile",
            complete: false
          },
          {
            title: "Mass Adoption",
            description: "Accessibility to WAXP in WAX Cloud Wallet",
            complete: false
          }
        ]
      },
      about: {
        title: "About Us",
        description:
          "Founded by crypto pioneers William Quigley and Jonathan Yantis, WAX is the safest and most convenient way to create, buy, sell and trade both virtual and physical items — to anyone, anywhere in the world.</br></br>WAX was purposefully built to be the most complete, climate friendly NFT ecosystem in the industry for leading brands, artists, creators and developers looking to leverage the power of the blockchain.</br></br>Top brands (including Topps, Capcom, Atari, Funko, Lionsgate and more) depend on WAX to launch their NFT collections, while the most prolific creators and developers use WAX’s powerful suite of tools to create award-winning video games and dApps.</br></br>Since its inception in 2017, WAX has been coined “The King of NFTs”, but it’s so much more — WAX vIRL® technology is literally the future of digital commerce.",
        background: "white",
        backgroundMobile: "",
        button: [{ text: "learn more", outlined: false }],
        large: true,
        items: [
          {
            name: "William E. Quigley",
            role: "Co-Founder, WAX",
            image: "images/william.png",
            social: ["images/twitter-logo.svg", "images/everipedia-logo.svg"]
          },
          {
            name: "Jonathan Yantis",
            role: "Co-Founder, WAX",
            image: "images/jonathan.png",
            social: ["images/everipedia-logo.svg"]
          }
        ]
      },
      community: {
        title: "Join Our Community",
        description:
          "Sign up to get the latest WAX news, NFT releases and blockchain updates.",
        background: "",
        backgroundMobile: "",
        button: [{ text: "subscribe", outlined: false }],
        large: false
      },
      discord: {
        title: "Have additional questions?",
        description: "Contact us through Discord.",
        logoTop: "images/discord-logo.svg",
        background: "",
        backgroundMobile: "",
        button: [{ text: "contact us", outlined: false }],
        large: false
      },
      educational: {
        title: "Educational Resources",
        description:
          "Here are some helpful articles and videos from our community.",
        background: "white",
        backgroundMobile: "",
        button: [],
        large: false,
        items: [
          {
            title: "",
            image: "images/beginner.png",
            imageMobile: "images/beginner-mobile.png",
            video: "",
            button: "Read"
          },
          {
            title: "",
            image: "images/create-nft.png",
            imageMobile: "images/create-nft-mobile.png",
            video: "",
            button: "Read"
          },
          {
            title: "",
            image: "images/tokenomic.png",
            imageMobile: "images/tokenomic-mobile.png",
            video: "",
            button: "Read"
          },
          {
            title: "What is an NFT",
            image: "",
            imageMobile: "",
            video: "https://www.youtube.com/embed/0aNCmZ4UMNM?wmode=opaque",
            button: ""
          },
          {
            title: "How to create NFTs",
            image: "",
            imageMobile: "",
            video: "https://www.youtube.com/embed/Zb0h9Qa5nHI?wmode=opaque",
            button: ""
          },
          {
            title: "How to buy NFTs",
            image: "",
            imageMobile: "",
            video: "https://www.youtube.com/embed/IJ57U29dgto?wmode=opaque",
            button: ""
          }
        ]
      }
    };
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.app {
  background-image: url(/wax-io/images/background.jpg);
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-position: center center;

  margin-top: 56px;
  @include breakpoint(lg) {
    margin-top: 64px;
  }
}
</style>
