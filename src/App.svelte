<script lang="ts">
    import Link from './lib/Link.svelte';
import Page from './lib/Page.svelte';
    import PhoneBook from './lib/PhoneBook.svelte';
    import PlacedDossier from './lib/PlacedDossier.svelte';
    import PlacedPage from './lib/PlacedPage.svelte';
    import PostIt from './lib/PostIt.svelte';
</script>

<main>
    <PlacedPage key='p1' --page-color="#C9C77F" --page-margin="1em">
        <h2>L: Links</h2>
        <PhoneBook entries={[
            ['Admitted Student Portal', 'admissions.uci.edu', 'https://admissions.uci.edu/apply/applicant-portal.php'],
            ['UCI Email', 'uci.service-now.com', 'https://uci.service-now.com/sp?id=kb_article&sysparm_article=KB0012451'],
            ['UCI Canvas', 'https://canvas.eee.uci.edu/', true],
            ['UCI Zoom', 'https://uci.zoom.us/', true],
            ['Orientation Reservation System', 'https://dev.reserve.orientation.uci.edu/', true],
            ['Academic Testing Center', 'https://testingcenter.uci.edu/', true],
            ['University Registrar', 'https://reg.uci.edu/', true],
            ['Financial Aid and Scholarships', 'https://www.ofas.uci.edu/', true],
            ['Financial Services Students', 'https://fs.uci.edu/', true],
            ['Student Housing', 'https://housing.uci.edu/first-year/', true],
            ['Transportation and Distribution Services', 'https://parking.uci.edu/', true],
            ['ZOTKEY', 'https://zotkey.uci.edu/', true],
            ['First-Year Internet Required Training', 'https://first.uci.edu/', true],
            ['Student Health Center', 'https://shc.uci.edu/uci-student-health-center', true],
            ['Career Pathways', 'https://career.uci.edu/', true],
            ['CampusGroups', 'https://campusgroups.uci.edu/home_login', true],

        ]} />
    </PlacedPage>

    <PlacedDossier key="d1" title="Classroom Tips" --dossier-translate="6px 8px">
        <h2 class="dossier-title" slot="cover">Classroom Tips</h2>

        <svelte:fragment slot="left">
            <PostIt --postit-color="#cb74f7" --postit-translate="5em 8em" --postit-rotate="3deg">
                <h3>Other Takeaways</h3>
                <ul>
                    <li>Reminder to interact with professors and go to office hours</li>
                    <li>Don't Cram</li>
                </ul>
            </PostIt>
            <PostIt --postit-color="#f2ffa0" --postit-translate="6em 2em" --postit-rotate="-1deg">
                <div class="small">
                    <h3>Video</h3>
                    <Link href="https://uci.yuja.com/V/Video?v=10482844&node=45880181&a=144135023" />
                    <h3>Unit</h3>
                    <Link href="https://canvas.eee.uci.edu/courses/65187/pages/module-1-navigating-the-university" />
                </div>
            </PostIt>
        </svelte:fragment>

        <Page>
            <h3>Timestamps</h3>
            <ul>
                <li><code>09:02</code> Syllabus</li>
                <li><code>13:06</code> <mark>Preparing for Class</mark></li>
                <li><code>14:48</code> <mark>Come to class in person</mark></li>
                <li><code>24:27</code> Working with fellow students</li>
                <li><code>30:17</code> <mark>Asking professors questions</mark></li>
                <li><code>34:26</code> <mark>Feedback</mark></li>
                <li><code>36:01</code> <mark>Office Hours<mark></li>
                <li><code>42:07</code> TAs and LAs</li>
                <li><code>46:30</code> Common Mistakes</li>
                <li><code>48:51</code> Imposter Syndrome</li>
                <li><code>54:09</code> Advice</li>
            </ul>
        </Page>
    </PlacedDossier>

    <PlacedDossier key="d2" title="Time Management" --dossier-translate="-6px 4px">
        <h2 class="dossier-title" slot="cover">Time Management</h2>

        <Page>
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

        <PostIt --postit-color="#74f7a8" --postit-translate="9em 16em" --postit-rotate="-6deg" slot="left">
            <h3>List of strategies</h3>
            <ul>
                <li>Spaced Practice</li>
                <li>Retrieval Practice</li>
                <li>Interleaving</li>
                <li>Dual Coding</li>
            </ul>
        </PostIt>

        <Page>
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
        
        <Page slot="left">
            <div class="small">
                <h3>Writing habits</h3>

                <h4>What kinds of setup, materials, or items on hand do you need to write comfortably?</h4>
                <p>I've found this out rather late but I think I write (for first drafts) best with pencil and paper. It's more tactile (which helps... something?) and it feels like there's less pressure to get everything right the first time since everything is going to be a bit messy anyway. Sometimes snacks help but mainly to keep me awake when I'm tired. Occasionally if I'm really stuck I grab a chair and sit out on the balcony at night, which both completely eliminates distractions and gives me an incentive to work faster (it's cold outside).</p>

                <h4>What time of day are you most productive when you're writing something?</h4>
                <p>I believe it is mornings and early evenings. I usually have plenty of energy in the mornings and in the evenings dinner provides a refresh, while in the afternoon I'm often tired from classes and during summer it's hot, and in later evening I'm too tired to concentrate.</p>

                <h4>Describe your ideal writing environment. Is it quiet and serene, or do you prefer a bit of background noise?</h4>
                <p>I'm not actually sure. I usually work in quiet environment because my family is not very loud (and listening to music doesn't seem to help me), so I don't know how I perform environment with noise. This is something to experiment with at UCI.</p>
            </div>
        </Page>

        <Page>
            <div class="small">
                <h3>Reflection & planning</h3>
                <h4>First, in a few sentences, identify what you feel are your top 3 concerns, skills, or areas of writing that you want to improve in your first few quarters at UCI.</h4>
                <ul>
                    <li>This has been addressed by the course already, but trying to make the first draft perfect (or even just better than it has to be). This ultimately makes me get stuck staring at the page and trying to squeeze out something or anything to write. By the time I actually do finish my first draft there's not a lot of time left to revise, reinforcing these tendencies.</li>
                    <li>My conclusions often don't sound conclusive. I know the theory (summarize, restate claim, application) but it still ends up feeling forced/templated or just weak.</li>
                    <li>I know when hooks sound unnatural, but it's still hard for me to find a hook that does sound natural and is effective.</li>
                </ul>
                
                <h4>Next, spend a few sentences answering this question: How will you try to address or deal with these concerns in your writing? What resources might you take advantage of or plan to use to improve on these areas of your writing?</h4>
                <p>To deal with these concerns, I can always come back to the resources in this unit and visit the UCI writing center. I can also go to office hours for my writing professor and get feedback and advice from my friends/peers. Additionally, some of my friends are doing small creative writing activities for fun during the summer that I might join to try and sharpen up before school starts.</p>
                
                <h4>Now, review your classes for the current or upcoming quarter. Which classes do you expect will have substantial writing assignments?</h4>
                <p>My schedule is still subject to change, but currently my comparative literature class will likely have the most writing, as an English/literature class. The next class likely to have a lot of writing is Games & Society, as we might have to analyze and justify the connections between games and society.</p>
            </div>
        </Page>
    </PlacedDossier>
</main>

<style>
    main {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
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
    }

    code {
        font-size: 1.3em;
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
</style>
