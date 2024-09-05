<script lang="ts">
    import "@fontsource/indie-flower";
    import "@fontsource/special-elite";

    import article1 from './assets/article1.png';
    import article2 from './assets/article2.png';
    import article3 from './assets/article3.png';

    import Link from './lib/Link.svelte';
    import Page from './lib/Page.svelte';
    import PhoneBook from './lib/PhoneBook.svelte';
    import PlacedDossier from './lib/PlacedDossier.svelte';
    import PlacedPage from './lib/PlacedPage.svelte';
    import PostIt from './lib/PostIt.svelte';
</script>

<main>
    <PlacedPage key='p2' --page-margin="1em">
        <div class="official">
            <h1>NOTICE: PRIVATE INVESTIGATION DOCUMENTS</h1>
            <p>Click pages and dossiers to exmaine them</p>
            <p>All URLs are linked</p>
            <p>Best viewed fullscreen</p>
        </div>
    </PlacedPage>

    <PlacedPage key='p1' --page-color="#C9C77F" --page-margin="1em">
        <h2>L: Links</h2>
        <PhoneBook entries={[
            ['ANTrepreneur Center', 'https://antrepreneur.uci.edu/', true],
            ['Academic Testing Center', 'https://testingcenter.uci.edu/', true],
            ['Admitted Student Portal', 'admissions.uci.edu', 'https://admissions.uci.edu/apply/applicant-portal.php'],
            ['Advising Offices', 'https://academicadvising.uci.edu/offices/', true],
            ['Campus Recreation', 'https://www.campusrec.uci.edu/', true],
            ['CampusGroups', 'https://campusgroups.uci.edu/home_login', true],
            ['Career Pathways', 'https://career.uci.edu/', true],
            ['Center for Excellence in Writing and Communication', 'https://writingcenter.uci.edu/', true],
            ['Center for Student Leadership', 'https://studentleadership.uci.edu/', true],
            ['Counseling Center', 'https://counseling.uci.edu/', true],
            ['Cross-Cultural Center', 'https://ccc.uci.edu/', true],
            ['Financial Aid and Scholarships', 'https://www.ofas.uci.edu/', true],
            ['Financial Services Students', 'https://fs.uci.edu/', true],
            ['Learning & Academic Resource Center (LARC)', 'https://larc.uci.edu/', true],
            ['Office of Campus Organizations and Volunteer Programs', 'https://covp.uci.edu/', true],
            ['Peer Academic Advisors', 'https://academicadvising.uci.edu/paa/', true],
            ['Student Health Center', 'https://shc.uci.edu/', true],
            ['Student Housing', 'https://housing.uci.edu/first-year/', true],
            ['Student Life & Leadership', 'https://studentlife.uci.edu/', true],
            ['Student Success Initiatives (SSI)', 'https://ssi.uci.edu/', true],
            ['Student Wellness & Health Promotion', 'https://studentwellness.uci.edu/', true],
            ['Study Abroad Center', 'https://studyabroad.uci.edu/', true],
            ['Transportation and Distribution Services', 'https://parking.uci.edu/', true],
            ['UCI Canvas', 'https://canvas.eee.uci.edu/', true],
            ['UCI Email', 'uci.service-now.com', 'https://uci.service-now.com/sp?id=kb_article&sysparm_article=KB0012451'],
            ['UCI Zoom', 'https://uci.zoom.us/', true],
            ['Undergraduate Research Opportunities Program (UROP)', 'https://urop.uci.edu/', true],
            ['University Registrar', 'https://reg.uci.edu/', true],
            ['Wellness, Health & Counseling', 'whcs.uci.edu/...', 'https://whcs.uci.edu/do-you-need-help/campus-assist-list'],
            ['ZOTKEY', 'https://zotkey.uci.edu/', true],

        ]} />
    </PlacedPage>

    <PlacedDossier key="d1" title="Classroom Tips" --dossier-translate="6px 8px">
        <h2 class="dossier-title" slot="cover">Classroom Tips</h2>

        <svelte:fragment slot="left">
            <PostIt --postit-color="#cb74f7" --postit-left="5em" --postit-top="8em" --postit-rotate="3deg">
                <h3>Other Takeaways</h3>
                <ul>
                    <li>Reminder to interact with professors and go to office hours</li>
                    <li>Don't Cram</li>
                </ul>
            </PostIt>
            <PostIt --postit-color="#dff453" --postit-left="18em" --postit-top="25em" --postit-rotate="-1deg">
                <div class="small">
                    <h3>Video</h3>
                    <Link href="https://uci.yuja.com/V/Video?v=10478580&node=45858755&a=58110704" />
                    <h3>Unit</h3>
                    <Link href="https://canvas.eee.uci.edu/courses/65187/pages/module-1-navigating-the-university" />
                </div>
            </PostIt>
        </svelte:fragment>

        <Page typewriter>
            <h3>Timestamps</h3>
            <ul>
                <li>09:02 Syllabus</li>
                <li>13:06 <mark>Preparing for Class</mark></li>
                <li>14:48 <mark>Come to class in person</mark></li>
                <li>24:27 Working with fellow students</li>
                <li>30:17 <mark>Asking professors questions</mark></li>
                <li>34:26 <mark>Feedback</mark></li>
                <li>36:01 <mark>Office Hours<mark></li>
                <li>42:07 TAs and LAs</li>
                <li>46:30 Common Mistakes</li>
                <li>48:51 Imposter Syndrome</li>
                <li>54:09 Advice</li>
            </ul>
            <p style="font-family: 'Indie Flower';">(I highlighted the parts I found most relevant)</p>
        </Page>
    </PlacedDossier>

    <PlacedDossier key="d2" title="Time Management" --dossier-translate="-6px 4px">
        <h2 class="dossier-title" slot="cover">Time Management</h2>

        <svelte:fragment slot="left">
            <PostIt --postit-color="#62f7e6" --postit-left="5em" --postit-top="12em" --postit-rotate="2deg">
                <Link href="https://canvas.eee.uci.edu/courses/65187/pages/module-4-time-management" />
            </PostIt>

            <a class="article-container" target="_blank" href="https://docs.google.com/presentation/d/e/2PACX-1vRB8y6Xvsx3dv5YZjHo_kdLJtY4TNFDPDyrIXtY07Kv39DuG711JNT93gm5br0dGgrvNmIO2LMEDQrT/pub?start=false&loop=false&delayms=3000#slide=id.g2c113ea9efb_0_12">
                <img class="article" src={article3} alt="Article 3" style:left="16em" style:bottom="1em" />
            </a>

            <div class="paperclip" style:rotate="180deg" style:top="auto" style:bottom="-4px" style:left="23em" />
        </svelte:fragment>

        <Page typewriter>
            <div class="indent">
                <h3>Notes</h3>
                <h4>Pomodoro</h4>
                <p>I've used this successfully in the past before. I have to be careful to make sure I use it as an aid and not a crutch. It doesn't magically solve all my problems, it just guides me in taking brakes and pacing.</p>
                <h4>Time Blocking</h4>
                <p>I've tried this in the past but I never really end up sticking to the schedule very well. The schedule isn't very helpful if it always gets shifted anyway.</p>
                
                <h4>Eat The Frog</h4>
                <p>This helps me a lot. I also like to call it "precedence": Starting the day (or time period) off by being productive successfully sets a good precedence of productivity for the rest of the day. I've recently started finishing all my chores before starting homework because otherwise I worry about chores the whole time I'm doing homework</p>
                
                <h4>Eisenhower Matrix</h4>
                <p>This seems like just a more complicated way of setting priorities, so I don't see a whole lot of value since I can already prioritize fairly well.</p>
            </div>
        </Page>
    </PlacedDossier>

    <PlacedDossier key="d3" title="Study Strategies" --dossier-translate="0 -3px">
        <h2 class="dossier-title" slot="cover">Study Strategies</h2>

        <svelte:fragment slot="left" let:open>
            <PostIt --postit-color="#74f7a8" --postit-left="5em" --postit-top="28em" --postit-rotate="-6deg">
                <h3>List of strategies</h3>
                <ul>
                    <li>Spaced Practice</li>
                    <li>Retrieval Practice</li>
                    <li>Interleaving</li>
                    <li>Dual Coding</li>
                </ul>
            </PostIt>
            
            <!-- svelte-ignore a11y-media-has-caption -->
            <video class="video1" src="https://josiahfu.github.io/dna.webm" loop controls autoplay={open} muted preload="metadata"></video>

            <PostIt --postit-color="#6291f7" --postit-left="24em" --postit-top="20em" --postit-rotate="2deg">
                <p>&#11025; A previous project I made for studying , an example of dual coding</p>
                <p>
                    <Link href="https://canvas.eee.uci.edu/courses/65187/pages/module-5-study-and-learning-strategies" />
                </p>
            </PostIt>
            <div class="paperclip" style:left="27em" />

        </svelte:fragment>

        <Page typewriter>
            <div class="indent">
                <h3>Chosen Strategies</h3>

                <h4>Putting away notes and writing/diagramming out everything (Retrieval/Dual Coding)</h4>
                <p>I will include this as one of the review strategies I use when preparing for quizzes and tests, or when I just need to refresh my knowledge.</p>
                <p>I can use paper, software like google drawings, or some other medium like a graphing calculator to write out all my knowledge. It's important to have a visual/spatial element as this improves connection-making between ideas.</p>

                <h4>Spaced Practice</h4>
                <p>I will set consistent days each week to spend studying, even when there is no test or exam in the immediate feature. I will identify the locations and times of the day I study best. I will review past material and read ahead for future material. I will aim to determine times and location by end of week 3 of the first quarter.</p>
            </div>
        </Page>
    </PlacedDossier>

    <PlacedDossier key="d3" title="Writing"  --dossier-translate="-4px -4px">
        <h2 class="dossier-title" slot="cover">Writing</h2>
        
        <svelte:fragment slot="left">
            <a class="article-container" href="https://canvas.eee.uci.edu/courses/65187/files/27477491?wrap=1" target="_blank">
                <img class="article" src={article1} alt="Article 1" style:top="1em" style:left="4em" />
            </a>
            <a class="article-container" href="https://canvas.eee.uci.edu/courses/65187/files/27477508?wrap=1" target="_blank">
                <img class="article right" src={article2} alt="Article 2" style:top="1.5em" style:left="16em" />
            </a>
            <div class="paperclip" style:left="19em" />
            <PostIt --postit-color="#7e62f7" --postit-left="4em" --postit-top="32em" --postit-rotate="2deg">
                <Link href="https://canvas.eee.uci.edu/courses/65187/pages/module-6-academic-writing-and-communication" />
            </PostIt>
            <PostIt --postit-color="#b9f762" --postit-left="13em" --postit-top="28em" --postit-rotate="-5deg">
                <p>
                    These were good articles, in particular the one about first drafts was actually kind of liberating for me and it helped me on another part of the UNISTU coursework.
                </p>
            </PostIt>
        </svelte:fragment>

        <Page>
            <div class="small worksheet">
                <h3>Reflection & planning</h3>

                <h4>What kinds of setup, materials, or items on hand do you need to write comfortably?</h4>
                <p>I've found this out rather late but I think I write (for first drafts) best with pencil and paper, partially because there's less pressure to get everything right the first time. Sometimes snacks help but mainly to keep me awake when I'm tired. Occasionally if I'm really stuck I grab a chair and sit out on the balcony at night, which both completely eliminates distractions and gives me an incentive to work faster (it's cold outside).</p>

                <h4>What time of day are you most productive when you're writing something?</h4>
                <p>I believe it is mornings and early evenings. I usually have plenty of energy in the mornings and in the evenings dinner provides a refresh, while in the afternoon I'm often tired from classes and during summer it's hot, and in later evening I'm too tired to concentrate.</p>

                <h4>Describe your ideal writing environment. Is it quiet and serene, or do you prefer a bit of background noise?</h4>
                <p>I'm not actually sure. I usually work in quiet environment because my family is not very loud (and listening to music doesn't seem to help me), so I don't know how I perform environment with noise. This is something to experiment with at UCI.</p>

                <h4>In a few sentences, identify what you feel are your top 3 concerns, skills, or areas of writing that you want to improve in your first few quarters at UCI.</h4>
                <ul>
                    <li>This has been addressed by the course already, but trying to make the first draft perfect (or even just better than it has to be). This ultimately makes me get stuck staring at the page and trying to squeeze out something or anything to write. By the time I actually do finish my first draft there's not a lot of time left to revise, reinforcing these tendencies.</li>
                    <li>My conclusions often don't sound conclusive. I know the theory (summarize, restate claim, application) but it still ends up feeling forced/templated or just weak.</li>
                    <li>I know when hooks sound unnatural, but it's still hard for me to find a hook that does sound natural and is effective.</li>
                </ul>
            </div>
        </Page>
    </PlacedDossier>
</main>

<style>
    main {
        /* display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center; */

        display: grid;
        grid-template-columns: auto auto auto;
        place-content: center;
        padding: 3em;

        gap: 3em;
        height: 100vh;
    }

    .dossier-title {
        color: red;
        display: inline-block;
        border: 0.25em solid red;
        border-radius: 0.5em;
        padding: 0.5em;
        place-self: center;
        rotate: 30deg;
        font-size: 3em;
        font-family: 'Special Elite', 'Courier New', Courier, monospace;
    }

    h3 {
        text-align: center;
        margin: 0.5em 0;
    }

    h4 {
        margin: 0.5em 0;
    }

    p {
        margin: 0.5em 0;
        font-size: var(--p-font-size);
        margin-left: var(--p-indent);
    }

    .indent p {
        margin-left: 2em;
    }

    .small {
        display: contents;
        font-size: 0.8em;
    }

    .small h3 {
        margin: 0.1em 0;
    }

    .worksheet p, .worksheet li {
        font-family: 'Indie Flower', cursive;
    }

    .article {
        position: absolute;
        width: 20em;
    }

    .article-container {
        display: contents;
    }

    .paperclip {
        height:6em;
        width:2em;
        border:4px solid rgb(53, 53, 53);
        border-radius:1em;
        box-sizing: border-box;
        position: absolute;
        top: -4px;
        clip-path: polygon(
            0 0,
            100% 0,
            100% 4px,
            50% 4px,
            50% 25%,
            100% 25%,
            100% 100%,
            0 100%
        );
    }

    .video1 {
        position: absolute;
        left: 4em;
        top: 2em;
        width: 30em;
    }
    
    .video1:not(:fullscreen) {
        rotate: 2deg;
    }

    .official {
        display: contents;
        text-align: center;
        font-size: 2em;
        font-family: 'Special Elite', 'Courier New', Courier, monospace;
    }

    .official h1 {
        font-size: 1em;
        margin: 2em;
    }
</style>
