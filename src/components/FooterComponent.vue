<script>
import FooterLinksCol from './FooterLinksCol.vue';

export default {
  data() {
    return {
        shopLocatorClass:'',
        footerItems:[
            {
                name: 'digital comics',
                src:'../assets/img/buy-comics-digital-comics.png'
            },
            {
                name: 'dc merchandise',
                src:'../assets/img/buy-comics-merchandise.png'
            },
            {
                name: 'subscriptions',
                src:'../assets/img/buy-comics-subscriptions.png'
            },
            {
                name: 'comic shop locator',
                src:'../assets/img/buy-comics-shop-locator.png'
            },
            {
                name: 'dc power visa',
                src:'../assets/img/buy-dc-power-visa.svg'
            }
        ],
		footerSocialIcons:[
			{
                name: 'facebook',
                src:'../assets/img/footer-facebook.png'
            },
			{
                name: 'twitter',
                src:'../assets/img/footer-twitter.png'
            },
			{
                name: 'youtube',
                src:'../assets/img/footer-youtube.png'
            },
			{
                name: 'pinterest',
                src:'../assets/img/footer-pinterest.png'
            },
			{
                name: 'periscope',
                src:'../assets/img/footer-periscope.png'
            },
		],
		footerInfo:[
			{
				title: 'DC COMICS',
				links:[
					'Characters',
					'Comics',
					'Movies',
					'Tv',
					'Games',
					'Videos',
					'News'
				]
			},
			{
				title: 'SHOP',
				links:{
					shopdc: 'Shop DC',
					shopDcColl: 'Shop DC Collectibles'
				}
			},
			{
				title: 'DC',
				links:{
					terms: 'Terms Of Use',
					privacy: 'Privacy Policy (New)',
					adChoices: 'Ad Choices',
					advertising: 'Advertising',
					jobs: 'Jobs',
					subscriptions: 'Subscriptions',
					talent: 'Talent Workshops',
					certificates: 'CPSC certificates',
					ratings: 'Ratings',
					shop: 'Shop Help',
					contactUs: 'Contact Us'
				}
			},
			{
				title: 'SITES',
				links:{
					dc: 'DC',
					madMagazine: 'Mad Magazine',
					dcKids: 'DC Kids',
					dcUniverse: 'DC Universe',
					dcVisa: 'DC Power Visa'
				}
			},
		]
      
    };
    },
	components:{
		FooterLinksCol
	},
    methods:{
        getImgPath: function(src) {
          return new URL(`${src}`, import.meta.url).href
        },
    },
}

</script>

<template>
    <section class="footer-items">
      <div class="container">
            <div class="items-row">

                <div class="single-item" v-for="singleItem in footerItems" :key="singleItem" :class="singleItem.name == 'comic shop locator' ? 'shop-locator' : ''">
                    <img :src="getImgPath(singleItem.src)" alt="">
                    <h3>{{ singleItem.name }}</h3>
                </div>

            </div>
      </div>
    </section>

    <section class="footer-info">
      <div class="container">
        <nav>
			<div>
				<FooterLinksCol
				:singleInfo="footerInfo[0]"
				:title="footerInfo[0].title">
				</FooterLinksCol>

				<FooterLinksCol
				:singleInfo="footerInfo[1]"
				:title="footerInfo[1].title">
				</FooterLinksCol>
			</div>
			<FooterLinksCol
			:singleInfo="footerInfo[2]"
			:title="footerInfo[2].title">
			</FooterLinksCol>

			<FooterLinksCol
			:singleInfo="footerInfo[3]"
			:title="footerInfo[3].title">
			</FooterLinksCol>

        </nav>
       
      </div>
    </section>

    <section class="footer-socials">
      <div class="container">
        <div>
          <button>Sign up now!</button>

          <div class="social-links">
            <h3>Follow Us</h3>
          
            <div class="social-icon" v-for="(socialIcon, socialIconIndex) in footerSocialIcons" :key="socialIconIndex">

				<img :src="getImgPath(socialIcon.src)" :alt="socialIcon.name">

			</div>

          </div>
         
        </div>
        
      </div>
    </section>
</template>


<style lang="scss" scoped>
.container{
  width: 1140px;
  margin: 0 auto;
}
footer{
    width: 100%;
    border: 1px solid black;

    section{
    
        &.footer-items{
            background-color: #2087EE;
            padding: 20px 0;

            .items-row{
                display: flex;
                justify-content: space-between;
            }

            h3{
                display: inline-block;
                text-transform: uppercase;
                color: white;
                font-weight: 500;
                font-size: 13px;
                padding-right: 5px;
            }
            .single-item{
                display: flex;
                align-items: center;
                cursor: pointer;
                border-radius: 5px;

                &.shop-locator img{
                    height: 50px;
                    width: auto;
                }

			&:hover{
				background-color: rgba($color: #000000, $alpha: 0.3);
			}
              img{
                width: 50px;
                padding: 10px;
              }
            }
        }
        &.footer-info{
            background-image: url('../assets/img/footer-bg.jpg');
            background-size: cover;
            background-repeat: no-repeat;
            overflow: hidden;

            .container{
                position: relative;
				background-image: url('../assets/img/dc-logo-bg.png');
				background-position: right;
				background-repeat: no-repeat;
				padding: 20px 0px;
            }
            nav{
                display: flex;
                flex-wrap: wrap;

                > div{
                    margin: 0 20px;
                }
            }
            #bg-logo{
                position: absolute;
                top: 0;
                right: 0;
                transform: translate(0, -20%);
            }
			.SHOP{
				align-self: flex-end;
			}
        }
        &.footer-socials{
            background-color: #303030;
            padding: 20px 0;
            .container > div{
            display: flex;
            align-items: center;
            justify-content: space-between;

                button{
                    border: 2px solid #2087EE;
                    padding: 10px 20px;
                    text-transform: uppercase;
                    background-color: rgba($color: #000000, $alpha: 0.0);
                    color: white;
        
                    &:hover{
                    cursor: pointer;
                    background-color: rgba($color: #2087EE, $alpha: 0.4);
                    }
                }
        
                h3{
                    text-transform: uppercase;
                    color: #2087EE;
                    padding-right: 20px;
                }
                a{
                    color: #797979;
                    text-decoration: none;
                    margin: 0 10px;
                }
                .social-links{
                    display: flex;
                    align-items: center;
                }
				.social-icon{
					margin: 0 10px;
					cursor: pointer;

                    img:hover{
                        background-color: white;
                        border-radius: 50%;
                    }
				}
            }
        }
    }
}

</style>
 