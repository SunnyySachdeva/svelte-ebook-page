<script>
    import Button from "$lib/components/Button.svelte";
    import TwitterIcon from "$assets/icons/twitter.webp"
    import ChevronArrow from "$assets/icons/Chevron-down.svg"
const faqs = [
  {
    question: "What will I learn from this ebook?",
    answer:
      "This ebook provides a comprehensive guide to relocating to Spain, covering everything from securing the right visa and navigating Spain's legal system to finding the perfect place to live and integrating into the local culture. Whether you're moving for work, study, or retirement, this guide equips you with the essential knowledge and practical steps to make your transition as smooth as possible.",
  },
  {
    question: "Who is this ebook for?",
    answer:
      "This ebook is perfect for anyone considering a move to Spain, whether you're planning a short-term stay or a permanent relocation. It's designed for expats, retirees, students, and professionals who want to avoid common pitfalls and streamline their move. If you're looking for a detailed, step-by-step guide to help you every step of the way, this ebook is for you.",
  },
  {
    question: "How much does the ebook cost?",
    answer:
      "The ebook is priced at $10. This one-time purchase grants you immediate access to all the content, including detailed chapters, actionable checklists, and valuable resources that will save you time, money, and stress during your move to Spain.",
  },
  {
    question: "Is the information in the ebook up-to-date?",
    answer:
      "Yes, the ebook is regularly updated to reflect the latest changes in Spanish immigration laws, visa requirements, and other relevant information. The author, John Smith, stays on top of these updates to ensure that you're receiving the most accurate and current guidance available.",
  },
  {
    question: "Can I get a refund if I'm not satisfied?",
    answer:
      "Absolutely. We offer a 30-day money-back guarantee. If you feel that the ebook did not meet your expectations or didn't provide the value you were looking for, simply contact us within 30 days of your purchase, and we’ll issue a full refund—no questions asked.",
  },
];
  let buttonClicked = $state(-1)
  /**
	 * @param {number} index
	 */
  function clicked(index) {
    if (buttonClicked === index) {
        buttonClicked = -1
    } else {
        buttonClicked = index
    }

  }
</script>

<section class="faq-section">
    <h2 class=" mb-l ">Frequently Asked Questions</h2>
    <div>
        <ul>
            {#each faqs as faq, index}
            <button onclick={() => clicked(index)}>
                <li>
                    <div class="question">
                        <h3>{faq.question}</h3>
                        <img src={ChevronArrow} alt="expand arrow">
                    </div>    
                    <p class={buttonClicked === index ? "show": "hide"}>{faq.answer}</p>
                </li>
            </button>
            {/each}
        </ul>
    </div>
    <div class="bottom-section">
        <Button>Buy Now</Button>
        <p>Any other questions?</p>
        <p><a href="#">Hit me up on twitter <img class="twitter-icon" src={TwitterIcon} alt="Twitter Icon"></a></p>
    </div>
</section>

<style>
    .faq-section {
        margin: 100px 15% 40px 15%;
    }
    li {
        border-bottom: 1px solid black;
        padding-bottom: 10px;
    }
    h3 {
        padding: 10px 0;
    }
    button {
        text-align: left;
        width: 1300px;
        padding: 5px 0;
    }
    .question {
        display: flex;
        justify-content: space-between;
    }
    .twitter-icon {
        width: 20px;
    }
    .hide {
        display: none;
    }
    .show {
        display:block;
    }
    .bottom-section {
       display:flex;
       flex-direction: column;
       align-items: center;
    }
    a {
        text-decoration: underline;
        color: rgb(25, 173, 223);
    }
</style>