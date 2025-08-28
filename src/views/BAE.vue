<script>

import Stepper from 'primevue/stepper';
import StepList from 'primevue/steplist';
import StepPanels from 'primevue/steppanels';
import StepItem from 'primevue/stepitem';
import Step from 'primevue/step';
import StepPanel from 'primevue/steppanel';

</script>


<template>
    <div class="card">
        <Stepper value="1">
            <StepItem value="1">
                <Step>Candidate Details</Step>
                <StepPanel v-slot="{ activateCallback }">
                    <div class="flex flex-col h-48">
                        <div
                            class="p-2 border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-left items-center font-medium">
                            <table class="table-auto w-full border-collapse">
                                <tbody>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Full Name:
                                        </td>
                                        <td class="border border-transparent">John Smith</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Email:</td>
                                        <td class="border border-transparent">johnsmith@gmail.com</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">ID Type:</td>
                                        <td class="border border-transparent">Singaporean</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">ID Number:
                                        </td>
                                        <td class="border border-transparent">S1234567A</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Phone Number:
                                        </td>
                                        <td class="border border-transparent">98765432</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Home Address:
                                        </td>
                                        <td class="border border-transparent">123, ABC Road, Singapore 123456</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Qualified
                                            Person Number:</td>
                                        <td class="border border-transparent">QP1234567</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Relevant Legal
                                            Training: </td>
                                        <td class="border border-transparent">Yes</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                    <div class="py-6">
                        <Button label="Approve" severity="danger" icon="pi pi-check" iconPos="right" class="mx-2"></Button>
                        <Button label="Next" icon="pi pi-arrow-right" iconPos="right" @click="activateCallback('2')" />
                    </div>
                </StepPanel>
            </StepItem>
            <StepItem value="2">
                <Step>Payment &nbsp;<Button icon="pi pi-check" rounded /> </Step> 
                <StepPanel v-slot="{ activateCallback }">
                    <div class="flex flex-col">
                        <div
                            class="p-2 border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            <table class="table-auto w-full border-collapse">
                                <tbody>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Payment Type:
                                        </td>
                                        <td class="border border-transparent pb-4">Paynow</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Payment
                                            Evidence:
                                        </td>
                                        <td class="border border-transparent">
                                            <Image
                                                src="https://www.dbs.com.sg/personal/support/iwov-resources/dbs_ps3revamp/article-detail/images/paynow_transfer/mobile-5.png"
                                                alt="Image" width="250" />
                                        </td>
                                    </tr>
                                </tbody>
                            </table>

                        </div>
                    </div>
                    <div class="flex py-6 gap-2">
                        <Button label="Back" severity="secondary" @click="activateCallback('1')" />
                        <Button label="Reject" severity="danger" icon="pi pi-times" iconPos="right" class="mx-2"></Button>
                        <Button label="Next" icon="pi pi-arrow-right" iconPos="right" @click="activateCallback('3')" />
                    </div>
                </StepPanel>
            </StepItem>
            <StepItem value="3">
                <Step>Education </Step>
                <StepPanel v-slot="{ activateCallback }">
                    <div class="flex flex-col">
                        <div
                            class="p-2 border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            <table class="table-auto w-full border-collapse">
                                <tbody>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Tyoe of
                                            Degree:
                                        </td>
                                        <td class="border border-transparent">Bachelors</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">University
                                            Name:</td>
                                        <td class="border border-transparent">Singapore Management University</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Date Awarded:
                                        </td>
                                        <td class="border border-transparent">10 May 2025</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Ranking
                                            Vertification Document:
                                        </td>
                                        <td class="border border-transparent"><a
                                                href="https://mozilla.github.io/pdf.js/web/compressed.tracemonkey-pldi-09.pdf"
                                                target="_blank"
                                                style="color: blue; text-decoration: underline; font-weight: bold; cursor: pointer;">
                                                Click to view document
                                            </a>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">University
                                            Admission Document:
                                        </td>
                                        <td class="border border-transparent"><a
                                                href="https://mozilla.github.io/pdf.js/web/compressed.tracemonkey-pldi-09.pdf"
                                                target="_blank"
                                                style="color: blue; text-decoration: underline; font-weight: bold; cursor: pointer;">
                                                Click to view document
                                            </a>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Degree of 3
                                            Years:
                                        </td>
                                        <td class="border border-transparent">True</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Single Degree:
                                        </td>
                                        <td class="border border-transparent">True</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Affected By
                                            Covid: </td>
                                        <td class="border border-transparent">True</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Remote
                                            Learning Document: </td>
                                        <td class="border border-transparent"><a
                                                href="https://mozilla.github.io/pdf.js/web/compressed.tracemonkey-pldi-09.pdf"
                                                target="_blank"
                                                style="color: blue; text-decoration: underline; font-weight: bold; cursor: pointer;">
                                                Click to view document
                                            </a></td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                    <div class="py-6">
                        <Button label="Back" severity="secondary" @click="activateCallback('2')" />
                        <Button label="Approve" severity="danger" icon="pi pi-check" iconPos="right" class="mx-2"></Button>
                        <Button label="Next" icon="pi pi-arrow-right" iconPos="right" @click="activateCallback('4')" />
                    </div>
                </StepPanel>
            </StepItem>
            <StepItem value="4">
                <Step>Others </Step>
                <StepPanel v-slot="{ activateCallback }">
                    <div class="flex flex-col h-48">
                        <div
                            class="p-2 border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            <table class="table-auto w-full border-collapse">
                                <tbody>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Accomodation
                                            requirements:
                                        </td>
                                        <td class="border border-transparent">Yes</td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Accomodation
                                            Document:</td>
                                        <td class="border border-transparent"><a
                                                href="https://mozilla.github.io/pdf.js/web/compressed.tracemonkey-pldi-09.pdf"
                                                target="_blank"
                                                style="color: blue; text-decoration: underline; font-weight: bold; cursor: pointer;">
                                                Click to view document
                                            </a>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="font-bold border border-transparent whitespace-nowrap">Exemptionss:
                                        </td>
                                        <td class="border border-transparent">Yes</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                    <div class="py-6">
                        <Button label="Back" severity="secondary" @click="activateCallback('3')" />
                        <Button label="Approve" severity="danger" icon="pi pi-check" iconPos="right" class="mx-2"></Button>
                        <Button label="Submit"></Button>
                    </div>
                </StepPanel>
            </StepItem>
        </Stepper>
    </div>

    

    <div class="card flex justify-center">
        <Stepper value="1" linear class="basis-[50rem]">
            <StepList>
                <Step value="1">Header I</Step>
                <Step value="2">Header II</Step>
                <Step value="3">Header III</Step>
            </StepList>
            <StepPanels>
                <StepPanel v-slot="{ activateCallback }" value="1">
                    <div class="flex flex-col h-48">
                        <div
                            class="border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            Content I</div>
                    </div>
                    <div class="flex pt-6 justify-end">
                        <Button label="Next" icon="pi pi-arrow-right" @click="activateCallback('2')" />
                    </div>
                </StepPanel>
                <StepPanel v-slot="{ activateCallback }" value="2">
                    <div class="flex flex-col h-48">
                        <div
                            class="border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            Content II</div>
                    </div>
                    <div class="flex pt-6 justify-between">
                        <Button label="Back" severity="secondary" icon="pi pi-arrow-left"
                            @click="activateCallback('1')" />
                        <Button label="Next" icon="pi pi-arrow-right" iconPos="right" @click="activateCallback('3')" />
                    </div>
                </StepPanel>
                <StepPanel v-slot="{ activateCallback }" value="3">
                    <div class="flex flex-col h-48">
                        <div
                            class="border-2 border-dashed border-surface-200 dark:border-surface-700 rounded bg-surface-50 dark:bg-surface-950 flex-auto flex justify-center items-center font-medium">
                            Content III</div>
                    </div>
                    <div class="pt-6">
                        <Button label="Back" severity="secondary" icon="pi pi-arrow-left"
                            @click="activateCallback('2')" />
                    </div>
                </StepPanel>
            </StepPanels>
        </Stepper>
    </div>


</template>
