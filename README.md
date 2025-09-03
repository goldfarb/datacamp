# What is an iSchool?

_This is a project from the [CRDDS](https://www.colorado.edu/crdds/) [August 2025 Research Data Foundations Camp](https://cu-boulder-crdds.github.io/Research-Data-Foundations-Camp-2025-August/). The question "what is an Information School?" was prompted by a conversation I had during an orientation event with some faculty in CU Boulder's [example thereof](https://www.colorado.edu/cmdi/infoscience)._

****

For this project, I am interested in mapping, both geographically and disciplinarily, where the self-described Information Schools, and Information Science departments, are in the US and anglophone Canada. I am interested in places outside of this limited area, but am circumscribing the inquiry for linguistic, internet searching reasons.

As someone who is newly part of such a place, and with some but definitely limited understanding of the ecosystem, my sense is that there are places that could be called CS or Data Science, and places that are [GLAM](https://en.wikipedia.org/wiki/GLAM_(cultural_heritage)) oriented, and a few places like CU where we're doing technology & culture. I'm curious if there are other versions of Information School that I'm less aware of.

****

## List of examples

I am going to gather the list of iSchools and Information Science departments granting PhDs ~three~ two ways:

&#x2611; The list of [members](https://www.ischools.org/members) from [iSchools](https://www.ischools.org/)

&#x2611; The American Library Association (ALA) list of [accredited programs](https://www.ala.org/cfapps/lisdir/lisdir_search.cfm) and [programs with PhDs](https://www.ala.org/cfapps/lisdir/)

&#x1F6AB;  I had planned to include the list from the accursed College Board's [College Search](https://bigfuture.collegeboard.org/college-search/major/information-science?deg=doctoral&navId=gh-cs). However, a spot check of the first result, [Ferris State University](https://www.ferris.edu/), indicated that there was not an Information Science degree, let alone a doctoral degree, and I chose to proceed with two data sources.

&#x2610; The list extracted from the first one hundred google results for 'information science phd' `as part of a next step / future project`

### _Extracting the data_

   
#### from iSchools.org

_see the code blocks below_
My process was to use [Selenium](https://www.selenium.dev/) to copy the source code from the iSchools dot org member database, make it into structured data, and save only the schools in North America for further consideration

#### from ALA.org

For the ALA list of accredited programs and the programs with PhD, I copied the text from the sites and cleaned with a combination of regex in Sublime Text and some logic in a google sheet

### _Cleaning the data_

I chose to clean up the data from the iSchool member database and the ALA lists manually - given the number of schools in each (fewer than 100) I decided it made more sense to make sure all the names were standardized by as a human looking at a google sheet, rather than writing code to make sure everything was of the form `University of State City` (I'm looking at you, _`Albany, University at, SUNY`_ and _`University of North Carolina at Chapel Hill`_ among others)

Additionally, I chose to do a little internet research as a human - confirm which schools have a doctoral program, see what the degree closest to _Information Science_ is called, note when the program began if it is immediately clear, and so forth

### Considering the data

For the scope of the [microcredential](https://cu-boulder-crdds.github.io/Research-Data-Foundations-Camp-2025-August/content/wrap-up/microcredential.html), and to keep this project from continuing indefinitely and me never finishing it, I am interesting in determining the following:

1. How close are the iSchool and ALA list of PhD programs? Which schools are on one but not the other? Of the comprehensive list (any school that appears on either list), how many are affiliated with a library school, MLIS program, or similar? [note: it is possible that there is a university with an iSchool and a library program that is separate]
2. Which states and provinces don't have an information or library school?

### Next steps

I'm interested in building on this in several ways, including:
* Looking at the geographic distribution of these programs
* Looking more systematically at the 'others' - what other programs are in the information schools?
* What is a more comprehensive list of schools? I am using the list from iSchools dot org because it is preassembled [`no! bad!` using data because it is there rather than because it is what I want is a terrible practice, and I'm doing it for this exercise but _know_ what a sketchy choice it is]
* Consider if there is a reason that places choose to be *Information Schools* when it seems to me like they could just as easily call themselves Computer Science or Data Science or ... The program at Carnegie Mellon, for example, is in Information Systems & Management, which seems very far from what I think of as the focus of an iSchool. Why is the Georgia Tech [College of Computing](https://www.cc.gatech.edu/) part of iSchools.org?
* Talk to *people* - the faculty in the Information Science department, including those who started the place and many who studied or have taught at other information schools might have examples of places that are essentially ischools but the department is called something else
* When did information schools start going as `iSchools`, and where does it align with Apple's [general naming scheme](https://en.wikipedia.org/wiki/IMac)?

### Notes

* The ALA list includes a couple spots in Québec; so much for only anglophone Canada
* I didn't include territories in the US or Canada
* The [github hosted web version](https://goldfarb.github.io/datacamp/) treats some of the markdown differently than github itself; I am making formatting choices for the github README version.

****
The code as well as this README are in the [Jupyter notebook](https://github.com/goldfarb/datacamp/blob/main/ischools.ipynb)


***
### Outcomes

* The list from iSchool dot org includes 54 schools in United States of America and Canada

<details>
  <summary>There are 12 schools on the iSchools list that aren't included on the ALA's list of accredited programs</summary>

* (these are the information schools without library programs):

1. Carnegie Mellon University,
1. Cornell University,
1. George Mason University,
1. Georgia Tech,
1. Michigan State University,
1. Penn State University,
1. Rochester Institute of Technology,
1. University of California Berkeley,
1. University of California Irvine,
1. University of Cincinnati,
1. University of Colorado Boulder,
1. University of Maryland Baltimore County 

</details>

<details>
  <summary>There are 22 schools on the ALA list that aren't included from iSchools dot org:</summary>

1. CUNY Queens College,
1. Catholic University of America,
1. Chicago State University,
1. East Carolina University,
1. Emporia State University,
1. North Carolina Central University,
1. Old Dominion University,
1. Pennsylvania Western University Clarion,
1. Southern Connecticut State University,
1. St. Catherine University,
1. St. John's University,
1. Texas Woman's University,
1. University of Alberta,
1. University of Hawaii,
1. University of North Carolina Greensboro,
1. University of Ottawa,
1. University of Puerto Rico,
1. University of Rhode Island,
1. University of Southern California,
1. University of Southern Mississippi,
1. Valdosta State University,
1. Western University 
</details>

<details>
  <summary>There are 42 schools on both lists, from the ALA and iSchools:</summary>

1. Dalhousie University,
1. Dominican University,
1. Drexel University,
1. Florida State University,
1. Indiana University Bloomington,
1. Indiana University Indianapolis,
1. Kent State University,
1. Long Island University,
1. Louisiana State University,
1. McGill University,
1. Pratt Institute,
1. Rutgers University,
1. San Jose State University,
1. Simmons University,
1. State University of New York Albany,
1. State University of New York Buffalo,
1. Syracuse University,
1. University of Alabama,
1. University of Arizona,
1. University of British Columbia,
1. University of California Los Angeles,
1. University of Denver,
1. University of Illinois Urbana-Champaign,
1. University of Iowa,
1. University of Kentucky,
1. University of Maryland,
1. University of Michigan,
1. University of Missouri,
1. University of North Carolina Chapel Hill,
1. University of North Texas,
1. University of Oklahoma,
1. University of Pittsburgh,
1. University of South Carolina,
1. University of South Florida,
1. University of Tennessee Knoxville,
1. University of Texas Austin,
1. University of Toronto,
1. University of Washington,
1. University of Wisconsin Madison,
1. University of Wisconsin Milwaukee,
1. Université de Montréal,
1. Wayne State University 

</details>

* There are 76 total information schools, according to either iSchools dot org or the ALA.

<details>
  <summary>There are 22 states and provinces without a program on the ALA's accreditation list:</summary>
  
1. Alaska,
1. Arkansas,
1. Delaware,
1. Idaho,
1. Manitoba,
1. Maine,
1. Montana,
1. New Brunswick,
1. North Dakota,
1. Nebraska,
1. New Hampshire,
1. Newfoundland & Labrador,
1. New Mexico,
1. Nevada,
1. Oregon,
1. Prince Edward Island,
1. South Dakota,
1. Saskatchewan,
1. Utah,
1. Vermont,
1. West Virginia,
1. Wyoming 

</details>


* There aren't any states with information schools but no ALA accredited program.
