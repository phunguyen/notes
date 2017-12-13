# progress mask layout
var progressIndicatorElement = jQuery.progressIndicator({
	'message' : "Searching Charges",
	'position' : 'html',
	'blockInfo' : {
		'enabled' : true
	}
});
var progressIndicatorElement = jQuery.progressIndicator({'blockInfo' : {'enabled' : true}});
var aChargeBatch = chargeBatch.split(' - ');
var search_params = '[[["chargestatus","e","' + chargeStatus + '"],["batch_id","e","' + aChargeBatch[0] + '"],["batch_name","e","' + aChargeBatch[1] + '"]]]';
jQuery.ajax({
	url : "index.php?module=Charge&view=List&search_params=" + search_params,
	dataType : "html",
	success : function(data) {
		jQuery("#listViewContents").html(data);
		jQuery(".chzn-select").chosen();
		listInstance.registerEventsAjax();
		progressIndicatorElement.progressIndicator({'mode' : 'hide'});
	}
});

# modal popup
app.showModalWindow(data,{'text-align' : 'left'});
var modalContent = '<div class="modelContainer"><div class="modal-header contentsBackground"><button title="Close" type="button" data-dismiss="modal" aria-hidden="true" class="close">x</button><h3>Add new code</h3></div><form id="editCode" class="form-horizontal" method="POST"><div class="modal-body"><div class="row-fluid"><div class="control-group"><label class="control-label">Tax Name</label><div class="controls"><input class="span3" type="text" name="taxlabel" placeholder="Enter tax name" value="" /></div></div></div></div></div><div class="modal-footer quickCreateActions"><div class="pull-right cancelLinkContainer" style="margin-top:0px;"><a class="cancelLink" type="reset" data-dismiss="modal">Cancel</a></div><button class="btn btn-success" type="submit" name="saveButton"><strong>Save</strong></button></div></div>';
app.showModalWindow(modalContent, {'text-align' : 'left'}, false);

# modal popup VT7
app.helper.showProgress();
app.helper.hideProgress();
var content = '<div class="modal-dialog">\
	<div class="modal-content">\
		<div class="modal-header">\
			<div class="clearfix">\
				<div class="pull-right " ><button type="button" class="close" aria-label="Close" data-dismiss="modal"><span aria-hidden="true" class="fa fa-close"></span></button></div>\
				<h4 class="pull-left">Receive Shipment</h4>\
			</div>\
		</div>\
		<div class="modal-body">\
			<div class="quickCreateContent">\
				<table class="massEditTable table no-border">\
					<tr>\
						<td class="fieldLabel col-lg-2"><label class="muted pull-right">Campaign Name&nbsp; <span class="redColor">*</span> </label></td>\
						<td class="fieldValue col-lg-4" ><input id="Campaigns_editView_fieldName_campaignname" type="text" data-fieldname="campaignname" data-fieldtype="string" class="inputElement nameField" name="campaignname" value="" data-rule-required="true" /></td>\
						<td class="fieldLabel col-lg-2"><label class="muted pull-right">Assigned To&nbsp; <span class="redColor">*</span> </label></td>\
						<td class="fieldValue col-lg-4" ></td>\
					</tr>\
				</table>\
			</div>\
		</div>\
		<div class="modal-footer">\
			<center><button  class="btn btn-success" type="submit" name="saveButton"><strong>Save</strong></button><a href="#" class="cancelLink" type="reset" data-dismiss="modal">Cancel</a></center>\
		</div>\
	</div>\
</div>';
app.helper.showModal(content);

# unbind events
var detailContentsHolder = jQuery('div.contents');
detailContentsHolder.off('click', 'button.selectRelation');



# select record in the popup
function setReferenceFieldValue(layouts\vlayout\modules\Vtiger\resources\Edit.js:158)



# add x months to date
function addMonths (date, count) {
  if (date && count) {
    var m, d = (date = new Date(+date)).getDate()

    date.setMonth(date.getMonth() + count, 1)
    m = date.getMonth()
    date.setDate(d)
    if (date.getMonth() !== m) date.setDate(0)
  }
  return date
}


# top right notify
Vtiger_Helper_Js.showPnotify
D:\Work\Code\vtiger\vtigercrm65\resources\helper.js