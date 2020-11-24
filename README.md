# angular-stepper
Angular Material stepper

import {Component, OnInit, ViewChild} from '@angular/core';
import {DatasourceService} from './datasource.service';
// declare var $;


@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit  {

  public data = [
    {name: 'therichpost', email: 'therichpost@gmail.com', website:'therichpost.com'},
    {name: 'therichpost', email: 'therichpost@gmail.com', website:'therichpost.com'},
    {name: 'therichpost', email: 'therichpost@gmail.com', website:'therichpost.com'},
    {name: 'therichpost', email: 'therichpost@gmail.com', website:'therichpost.com'},
];
  title = 'angulardatatables';
  dtOptions: DataTables.Settings = {};
  ngOnInit() {
    this.dtOptions = {
      pagingType: 'full_numbers',
      pageLength: 10,
      processing: true
    };
}

}


   <table class="table table-striped table-bordered table-sm row-border hover" datatable [dtOptions]="dtOptions">
                      <thead>
                        <tr>
                          <th>Name</th>
                          <th>Email</th>
                          <th>Website</th>
                        </tr>
                      </thead>
                      <tbody>
                       <tr *ngFor="let group of data">
                             <td>{{group.name}}</td>
                             <td>{{group.email}}</td>
                             <td>{{group.website}}</td>
                         </tr>
                      </tbody>
                    </table>


 "styles": [
              "src/styles.scss",
              "node_modules/datatables.net-dt/css/jquery.dataTables.css",
              "node_modules/bootstrap/dist/css/bootstrap.min.css"
            ],
            "scripts": ["node_modules/jquery/dist/jquery.js",
              "node_modules/datatables.net/js/jquery.dataTables.js",
              "node_modules/bootstrap/dist/js/bootstrap.js"]
